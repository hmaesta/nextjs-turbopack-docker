## 1. Build the image using Turbopack
```
docker build . -t docker-experiment-turbopack
```


## 2. Move to Webpack
Add `--webpack` to package.json commands:
```
perl -i -pe '
  s/"dev":\s*"next dev"/"dev": "next dev --webpack"/;
  s/"build":\s*"next build"/"build": "next build --webpack"/;
' package.json
```
<sup>... or [edit package.json manually](https://nextjs.org/docs/app/api-reference/turbopack#using-webpack-instead)</sup>


## 3. Build the image using Webpack
```
docker build . -t docker-experiment-webpack
```

...

Compare results.