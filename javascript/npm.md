### NPM

**Script command line arugments**

In the Package.json scripts block:
```
"scripts": {
  "something": "curl http://$URL --output results.html"
}
```

command line:
`URL=www.sponebob.com npm run something`
