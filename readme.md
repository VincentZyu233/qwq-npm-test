## npm publish
```bash
npm init -y
proxychains4 npm login --registry https://registry.npmjs.org
# 在项目根目录创建.npmrc文件，写入：//registry.npmjs.org/:_authToken=npm_..... (npm网页上面申请的Access Token)
proxychains4 npm publish --registry https://registry.npmjs.org
```

# github action