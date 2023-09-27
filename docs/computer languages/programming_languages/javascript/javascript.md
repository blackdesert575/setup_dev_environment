# javascript

## basic

* [w3schools/JavaScript Tutorial](https://www.w3schools.com/js/)
* How to run Javascript?
    * [How To Add JavaScript to HTML](https://www.digitalocean.com/community/tutorials/how-to-add-javascript-to-html)
    * [How To Write Your First JavaScript Program](https://www.digitalocean.com/community/tutorials/how-to-write-your-first-javascript-program)
    * [How To Use the JavaScript Developer Console](https://www.digitalocean.com/community/tutorials/how-to-use-the-javascript-developer-console)
    * [How To Use the Node.js REPL](https://www.digitalocean.com/community/tutorials/how-to-use-the-node-js-repl)

## frameworks/packages/library

* [nvm](https://github.com/nvm-sh/nvm)
    * Node Version Manager - POSIX-compliant bash script to manage multiple active node.js versions
* [nodejs](https://nodejs.org/en)
    * Node.js® is an open-source, cross-platform JavaScript runtime environment.
    * [arch linux/node.js wiki pages](https://wiki.archlinux.org/title/node.js_)
* [react](https://zh-hant.legacy.reactjs.org/)
* [Next.js](https://nextjs.org/docs)
* [jquery](https://jquery.com/)
* [MDN/AJAX](https://developer.mozilla.org/en-US/docs/Web/Guide/AJAX)

## setting up dev enviroment

* setting up on Arch Linux

```shell
#install nvm via yay
yay -S nvm

#Add environment variable to your shell configuration
echo 'source /usr/share/nvm/init-nvm.sh' >> ~/.bashrc
source ~/.bashrc

#Verify Installation
nvm --version
command -v nvm

#Instal Active Long Term Support (LTS) node.js latest version via nvm
nvm install --lts
which node
node -v
which npm
npm --version


#usage with projects
npm init
npm install packages

##yarn?
#Node.js >=16.10
corepack enable
yarn && yarn start
```

## projects

* [todo-react](https://github.com/hong539/todo-react)