## npm publish
```bash
npm init -y
proxychains4 npm login --registry https://registry.npmjs.org
# 在项目根目录创建.npmrc文件，写入：//registry.npmjs.org/:_authToken=npm_..... (npm网页上面申请的Access Token)
proxychains4 npm publish --registry https://registry.npmjs.org
```

# github action
```bash
git init
git remote add origin git@github.com:VincentZyu233/qwq-npm-test.git

touch .gitignore
echo ".npmrc" >> .gitignore

git add .
git commit -m "chore: save changes before version bump"
npm version patch
git add .
git commit -m "pub qwq"

# 去github仓库设置，Secrets and variables -> Actions -> New repository secret， 名字是NPM_TOKEN， 内容是npm网站申请的npm_... 开头的字符
git push -u origin master
```