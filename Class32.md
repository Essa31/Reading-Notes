# Read: Class 32

## Django REST: Permissions

Permissions determine whether a request should be granted or denied access, but how permissions are determined?

### How permissions are determined:

Whenever the main body of a view is going to be called, there will be some checks on each permission in the list, and if any of them fails, one of the following exceptions will be raised:
- `exceptions.PermissionDenied`
- `exceptions.NotAuthenticated`

#### **Some situations of failed checks and what do they mean**: ([source](https://www.django-rest-framework.org/api-guide/permissions/#how-permissions-are-determined))

| Situation | Response |
|----------|---------|
| Request was authenticated, but the premission was denied | HTTP 403 Forbidden |
| Request was not authenticated, and the highest priority authentication class does not use `WWW-Authenticate` headers | HTTP 403 Forbidden |
| Request was not authenticated, and the highest priority authentication class does  use `WWW-Authenticate` headers | HTTP 401 Unauthorized, with an appropriate `WWW-Authenticate` |

### Object level permissions:

REST framework permissions offers developers object-level permissioning, which allows them to determine if a users are allowed to perform any action on a specific object or not, but these option comes with some limitations.

### Some API good references:

- `AllowAny`: this permission class allows unrestricted access.
- `IsAuthenticated`: this permission class is used to deny access for any unauthenticated user, and allow it otherwise.
- `IsAdminUser`: this permission class is used to deny any user access unless `user.is_staff` is set to `True`.
- `IsAuthenticatedOrReadOnly`: this permission class will only allow safe request methods, such as:
    - GET
    - HEAD
    - OPTIONS
- `DjangoModelPermissions`: this permission class is usually used with views that has `.queryset` property or `get_queryset()` method, and it will only allow the user to perform actions according to their permission level.
- `DjangoModelPermissionsOrAnonReadOnly`: this permission class is similar to `DjangoModelPermissions`, but the only difference is that it allows for read-only access for unauthenticated users
- `DjangoObjectPermissions`: this permission class allows per-object permissions on models.

## Things I want to know more about

- None.

## Resources

[sources1](https://www.django-rest-framework.org/api-guide/permissions/)

[sources2](https://codefellows.github.io/common_curriculum/prep_work/SQL)
