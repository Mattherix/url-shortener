# Contribuer

N'ayez pas peur de contribuer même si vous ne faites pas partie du groupe.

Ouvrez une issue à chaque fois que vous voulez parler d'un sujet. Une issue par sujet.

Aucune modification sur la branche principale, tous via des PR(Pull Request). Pour merge du code il faut minimum 1 review. Si votre PR à un conflit résolvez le en rebasant la branche principale dans la vôtre.

Avant de push vos changement mettez à jour votre branche via un `git pull --rebase`

## Convention sur les messages de commit

Nous utiliserons la convention décrite (içi)[https://dev.to/i5han3/git-commit-message-convention-that-you-can-follow-1709], c'est probablement la plus répendue.

Un commit par problème.
```
<type>(<scope>): <subject>
A deeper explanation about the commit
Fixes/Closes at the end of the commit will automatically close the related issue.

Fixes #33
```
Les 2 seul scope içi sont front et api