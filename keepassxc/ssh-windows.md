# Configure SSH Agent in KeePassXC on Windows

## Configure Windows SSH-Agent
- Start Windows PowerShell in Administrator mode
- Enable SSH Agent Service to start automtically (delayed). By default this service is disabeld
  ```
  Get-Service ssh-agent | Set-Service -StartupType AutomaticDelayedStart
  ```
- Start the SSH Agent Service
  ```
  Start-Service ssh-agent
  ```
- Check SSH Agent Service Status
  ```
  Get-Service ssh-agent
  ```

## Configure KeePassXC
- Open KeePassXC Application Settings (Tools > Settings or CTRL+, )
- Under SSH Agent activate `Enable SSH Agent integration`
- Set `Use OpenSSH`

# Using KeePassXC

> [!IMPORTANT]
> Under Windows do not activate `Require user confirmation when this key is used`. This setting is not supported in Windows SSH-Agent and will break the function (`Agent protocol error` will appear).

- Create a new entry in KeePassXC
- The SSH passphrase can be saved in the password field
- Under Advanced import the private SSH key and optional the public SSH file
- Under SSH Agent select the private key from the attached private SSH key
