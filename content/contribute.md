---
title: "Getting started with a pull request"
---

Ready to add yourself to the list of participants? To add our profile to https://nchlswhttkr.github.io/hacktoberfest-2019, we'll be making our pull request (abbreviated PR).

Before you begin, you will need a [GitHub account](https://github.com/join) and to have Git installed on your computer.

This tutorial will use the Git CLI, but you're welcome to use a [Git GUI client](https://git-scm.com/downloads/guis) or to use GitHub directly. We'll only be creating a single file with our PR.

<br/>

#### 1. Fork this repository

To start, we'll create a fork of the repo. You can do this by going to https://github.com/nchlswhttkr/hacktoberfest-2019/fork

Once GitHub has finished generating your fork you'll be redirected.

<br/>

#### 2. Clone it to your local machine

Next, we'll tell Git to make a clone of our forked repository. You can copy the URL of your repository from GitHub, or replace `your-username` with your username in the below example.

<!-- Thankfully Git knows we're referring to the .git resource -->

```sh
git clone https://github.com/your-username/hacktoberfest-2019
cd hacktoberfest-2019
```

<br/>

#### 3. Create your participant page

From inside the `hacktoberfest-2019` directory that you've cloned, we'll create new file to fill out your profile.

Inside the `/content/participants` directory, create a markdown file with your name (for example, `john-smith.md`). \
Inside this file you can write a little bit about yourself, don't forget to put your name in the title! Write a little about what you're studying, and add a link to your GitHub profile!

```txt
---
title: "Nicholas Whittaker"
---

Hi, I'm Nicholas! I'm a final year Computer Science student here at Monash!

My favourite language is Javascript, but I like to write Python, Go and C++ as well!

You can find me on GitHub at https://github.com/nchlswhttkr
```

Write a little about what you're studying, and add a link to your GitHub profile!

<br/>

#### 4. Commit and push your changes

After you've saved your participant file, you can stage and commit your changes with Git.

```sh
git add content/participants
git commit -m "Add me as a participant"
```

You can then push this back to your repository on GitHub.

```sh
git push
# Username for 'https://github.com': ...
# Password for 'https://username@github.com': ...
```

<br/>

:exclamation: :exclamation: :exclamation: If you get a "permission denied" error because you do not have "write access", have a look at the [troubleshooting help](#unable-to-push-changes)

<br/>

#### 5. Make a Pull Request

Once your commits have pushed, go can go back to GitHub to create a PR.

You may see a prompt to create a PR, or otherwise you can click on the **New pull request** button.

Give your PR a title and look at the changes you're submitting! \
If you want to double check, your PR should be coming from the `master` branch of your fork (`your-username/hacktoberfest-2019`) and should be targeting the `master` branch of the main repo (`nchlswhttkr/hacktoberfest-2019`).

<br/>

### 6. Check your Hacktoberfest progress

Head over to https://hacktoberfest.digitalocean.com/profile and sign in with your GitHub account to view your progress!

<br/>

---

<br/>

## Troubleshooting

<br/>

### Unable to push changes

```sh
git remote -v
```

If the URL is `https://github.com/nchlswhttkr/hacktoberfest-2019.git`, you may have accidentally cloned the main repo, and not your fork. Thankfully this can be easily fixed!

With this command, we tell Git to change where it sends pushes. Make sure to change `your-username` to your actual GitHub username

```sh
git remote set-url origin https://github.com/your-username/hacktoberfest-2019
git push
```
