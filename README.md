# Resume

## Dependancies

- [toml](https://github.com/gnprice/toml-cli): `cargo install --git https://github.com/gnprice/toml-cli.git`
- [hbs](https://github.com/keithamus/hbs-cli): `npm install hbs-cli -g`


## Usage

Convert the toml to json with `toml` and inject the json data into the template via handlebars cli `hbs`.

```sh
toml get resume.toml . | hbs -i -s -- ./theme/resume.template > ./resume.html
```
