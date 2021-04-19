# Resume

This repository stores and hosts my resume. Resume data is stored in resume.toml and follows the [jsonresume schema](https://jsonresume.org/schema/) with minor deviations.

## Dependancies

- [toml](https://github.com/gnprice/toml-cli): `cargo install --git https://github.com/gnprice/toml-cli.git`
- [jsonresume-theme-flat](https://github.com/dmmuir/jsonresume-theme-flat/blob/master/index.js): `cd ./themes/jsonresume-theme-flat && npm install`

## Usage

Convert the toml to json with `toml` and inject the json data into the template via handlebars with [jsonresume flat theme](https://github.com/erming/jsonresume-theme-flat) under `/themes/jsonresume-theme-flat/`.

### Build

```sh
toml get resume.toml . | node themes/jsonresume-theme-flat/index.js > ./index.html
```

### Publish

This resume is hosted by way of github pages. Add the ./index.html file to gh-pages branch and push the changes.

```sh
toml get resume.toml . | node themes/jsonresume-theme-flat/index.js > ./resume.html
git checkout gh-pages
mv resume.html index.html
git commit -am "Update resume"
git push
```
