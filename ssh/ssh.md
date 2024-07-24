# Create SSH Key
```
ssh-keygen -t ed25519 -C "your_email@domain.com"
```

> [!NOTE]
> For legacy systems that doesn't support the Ed25519 algorithm use RSA:
> ```
> ssh-keygen -t rsa -b 4096 -C "your_email@domain.com"
> ```

> [!TIP]
> For more information see https://docs.github.com/en/authentication/connecting-to-github-with-ssh/about-ssh
