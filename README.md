
### ko-requset
[![npm version](https://img.shields.io/npm/v/ts-loader.svg)](https://www.npmjs.com/package/ko-script)
[![Linux Build Status](https://travis-ci.org/TypeStrong/ts-loader.svg?branch=master)](https://npmjs.org/package/ko-script)


#### Install
```
yarn add ko-requset
npm install @dtux/ko-request
```
#### Usage
```
import { Fetch, Axios } from '@dtux/ko-request';
```
#### New http
```
const http = new Fetch({
	baseURL: '',
	initConfig: {
		headers: {}
	},
	reqIntercept: (config, url) => {
		// reqeset Intercept在这里添加loading、 配置token
		return config
	},
	resIntercept: (res, url) => {
		// response Intercept在这里关闭loading
		return Promise.resolve(res);
	}
});

http.get('/users')

```
