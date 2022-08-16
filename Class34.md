# Read: Class 34

## Configuring Django Settings: Best Practices

**Django developers may face a couple of issues when configuring their settings, some of these issues are**:

- *Different environments*
- *Sensitive data*
- *Sharing settings between team members*
- *Django settings are a Python code*

And that's why we are going to look at a couple of approaches in order to try and fix these issues.

### Setting Configuration Approaches:

- **settings_local.py**: which is a file that is used to extend the main `settings.py` without directly changing it.

    *Pros and Cons*

    And while this way is good as it's ignored by VCS, it raises some other problems like losing some of Django's environment settings as it's not in VCS, or having to create another file to share the default configurations with other developers.

- **A settings file for each environment**: which is an extension of the previous approach as you would create a folder that would host a bunch of files that manages different things, but it differs as it is in VCS.

    *Pros and Cons*

    This approach is good as it all the environments would be in VCS, and it would be easy to share between developers, but you'll need to find a way to handle secret passwords and tokens and it relays on inheritance, which would be somewhat hard to trace.

- **Environment variables**: it is used usually for sensitive data.

    *Pros and Cons*

    This approach is great as it separates code and configuration, allows you to have the same code for all environments and also does not use inheritance, but you'll still need to handle default configuration sharing between developers

### Django Settings: Best practices

- Settings should be kept in environment variables.
- Production configuration should have default values.
- Avoid putting sensitive settings in VCS.
- Try to split settings into groups.

## SSH

### Definition: ([source](https://www.hostinger.com/tutorials/ssh-tutorial-how-does-ssh-work#:~:text=SSH%2C%20or%20Secure%20Shell%20Protocol%2C%20is%20a%20remote%20administration%20protocol%20that%20allows%20users%20to%20access%2C%20control%2C%20and%20modify%20their%20remote%20servers%20over%20the%20internet.))

Secure Shell Protocol (SSH) is a remote administration protocol that allows users to access, control, and modify their remote servers over the internet.

This protocol was created to make sure that all comunication to and from the remote server is encrypted and protected.

### SSH Encryption Techniques:

- **Symmetrical encryption**: this kind of encryption relays on a **secret key** that everyone who possess it can read the data.

- **Asymmetrical encryption**: this kind of encryption relays on two keys *public* and *private* and their both used to decrypt the data. The public key can be used by anyone to encrypt the data, but only the users with the data's private key can decrypt it.

- **Hashing**: this kind is made to not be decrypted as it uses some way of encryption that has no trends to make sure that it can't be exploited. 

## Things I want to know more about

- None.

## Resources

[sources1](https://djangostars.com/blog/configuring-django-settings-best-practices/)

[sources2](https://www.hostinger.com/tutorials/ssh-tutorial-how-does-ssh-work)

