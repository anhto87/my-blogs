

# Multi SSH-Key for GitHub account
## create different public key
Jump to `~/.ssh` folder and type this command

`$ ssh-keygen -t rsa -C "your_email@youremail.com"`

Remember, the `console` will be ask you about something like this:

> Generating public/private rsa key pair.

> Enter file in which to save the key (/Users/macintosh/.ssh/id_rsa):[**enter_your_name_id_rsa_here**]

For example I will have one more key created:

    ~/.ssh/id_rsa_anhto87_github
Next, add this key to machine

`$ ssh-add ~/.ssh/id_rsa_anhto87_github`

Next, we will reset cached keys of Git
`$ ssh-add -D`

## Modify the `config` of git
You can skip this step in the case you had this file `~/.ssh/config`

Ok next, edit this file

    Host github-anhto87_github
        HostName github.com
        User git
        IdentityFile ~/.ssh/id_rsa_anhto87_github

Done. Give me your comment if your configuration not work.

Thanks,

	   
    

