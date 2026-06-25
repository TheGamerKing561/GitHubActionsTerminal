# GitHub Actions Terminal

# How to use

1- Fork this repository

2- Go to Repository settings -> Secrets and variables -> Actions

3- Create a new repository secret, name it "userpassword" and give it a value. This will be the password you will use for connection.

4- Go to Actions and choose "Remote Terminal Session" workflow.

5- Run the workflow

6- Wait until the workflow reaches the "Start Cloudflare Quick Tunnel" step, then your new tunnel link will be printed.

It looks something like this: random-words.trycloudflare.com

7- Download the Cloudflare Tunnel client on your device from [here](https://developers.cloudflare.com/cloudflare-one/networks/connectors/cloudflare-tunnel/downloads/).

8- Open a new terminal, then run this command:

```bash
cloudflared access tcp --hostname <link-to-tunnel> --url localhost:222
```
**DO NOT CLOSE THIS TERMINAL WINDOW**

9- Connect to SSH by using your favorite SSH client to localhost (port 2222) with the username "runner" and the password you entered in the "Secrets and variables" page.
