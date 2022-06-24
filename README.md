# React before after slider component

Simple slider component for comparing images before and after.

[![screencast demo](./screencast.gif)](./screencast.gif)

## Demo

https://mridul2820.github.io/react-after-before-slider/

## Build

npm run build:npm

## Basic usage

```
npm i react-after-before-slider --save
```

Then use it in your app:

```jsx
import React from 'react';
import ReactBeforeSliderComponent from 'react-after-before-slider';
import 'react-after-before-slider/dist/build.css';

const FIRST_IMAGE = {
  imageUrl: 'https://example.com/.../some-image-1.jpg',
};
const SECOND_IMAGE = {
  imageUrl: 'https://example.com/.../some-image-2.jpg',
};

<ReactBeforeSliderComponent
  firstImage={FIRST_IMAGE}
  secondImage={SECOND_IMAGE}
/>;
```

## Props

| Attribute                 | Required | Type     | Default | Description                                                                          |
| ------------------------- | -------- | -------- | ------- | ------------------------------------------------------------------------------------ |
| `firstImage`              | true     | Image    |         | Image object with source url.                                                        |
| `secondImage`             | true     | Image    |         | Image object with source url.                                                        |
| `delimiterColor`          | false    | string   |         | Custom delimiter background color.                                                   |
| `currentPercentPosition`  | false    | number   | 50      | Start delimiter position. Or also the current position, if it will change in parent. |
| `className`               | false    | string   |         | Custom classname.                                                                    |
| `withResizeFeel`          | false    | boolean  | true    | Feeling to window resizing.                                                          |
| `onReady`                 | false    | function |         | On slider ready callback.                                                            |
| `onVisible`               | false    | function |         | On slider visible in viewport callback.                                              |
| `onChangePercentPosition` | false    | function |         | On delimiter position update callback. Has new position parameter.                   |
| `feelsOnlyTheDelimiter`   | false    | function | false   | Only the separator feels clicks. Not any zone of the component.                      |

## Specific Types

```ts
interface Image {
  imageUrl: string;
  alt?: string;
}
```
