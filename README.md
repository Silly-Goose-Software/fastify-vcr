# @silly-goose-software/fastify-vcr

[![npm package][npm-img]][npm-url]
[![Build Status][build-img]][build-url]
[![Downloads][downloads-img]][downloads-url]
[![Issues][issues-img]][issues-url]
[![Code Coverage][codecov-img]][codecov-url]
[![Commitizen Friendly][commitizen-img]][commitizen-url]
[![Semantic Release][semantic-release-img]][semantic-release-url]

> Record and replay HTTP requests that hit a certain route. Includes a single plugin that adds both the recorder and the admin controls.

## Reasoning

I've been working on quite a few webhook-based integrations with third-parties. One of the challenges is harvesting test data prior to switching stuff on. Ideally, one would want to enable the influx of webhook requests well before the rest of the implementation lands, as it'll help inform the design, the required validation, the expected workflow, etc.

But I haven't found a lot of tooling around this, especially not when I'm looking for the following requirements:

1. Persist HTTP requests to a certain route
2. List persisted HTTP requests
3. Replay a persisted HTTP request, marking it as replayed

Secondly, I'd like to play with Fastify's "Everything is a plugin" philosophy. I come out of a koa/express shop prior to my current gig, and Fastify is relatively new to me.

## Install

```bash
npm install @silly-goose-software/fastify-vcr
```

## Usage

```ts
import { myPackage } from '@silly-goose-software/fastify-vcr';

myPackage('hello');
//=> 'hello from my package'
```

## API

### myPackage(input, options?)

#### input

Type: `string`

Lorem ipsum.

#### options

Type: `object`

##### postfix

Type: `string`
Default: `rainbows`

Lorem ipsum.

[build-img]:https://github.com/yannickmeeus/@silly-goose-software/fastify-vcr/actions/workflows/release.yml/badge.svg
[build-url]:https://github.com/yannickmeeus/@silly-goose-software/fastify-vcr/actions/workflows/release.yml
[downloads-img]:https://img.shields.io/npm/dt/@silly-goose-software/fastify-vcr
[downloads-url]:https://www.npmtrends.com/@silly-goose-software/fastify-vcr
[npm-img]:https://img.shields.io/npm/v/@silly-goose-software/fastify-vcr
[npm-url]:https://www.npmjs.com/package/@silly-goose-software/fastify-vcr
[issues-img]:https://img.shields.io/github/issues/yannickmeeus/@silly-goose-software/fastify-vcr
[issues-url]:https://github.com/yannickmeeus/@silly-goose-software/fastify-vcr/issues
[codecov-img]:https://codecov.io/gh/yannickmeeus/@silly-goose-software/fastify-vcr/branch/main/graph/badge.svg
[codecov-url]:https://codecov.io/gh/yannickmeeus/@silly-goose-software/fastify-vcr
[semantic-release-img]:https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg
[semantic-release-url]:https://github.com/semantic-release/semantic-release
[commitizen-img]:https://img.shields.io/badge/commitizen-friendly-brightgreen.svg
[commitizen-url]:http://commitizen.github.io/cz-cli/
