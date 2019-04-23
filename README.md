# Redux
## Core

#### Mission

You have to develop a Redux app with React Native binding that will work in both iOS and Android platforms. For convenience we are only going to test the app in iOS iphone simulator. We expect you to fully understand the concept of redux and implement it in the project. Wen also require you to do the project with following parameters

* Project dashboard to show how you complete project features
* Git feature branches, commit message:
* Guideline: https://medium.com/@steveamaza/how-to-write-a-proper-git-commit-message-e028865e5791
* Example: https://github.com/facebook/react-native/commits/master
* A release with change note
* Installation instruction in Readme.md

---
#### Redux

Redux is a predictable state container for JavaScript apps.

Redux helps you write applications that behave consistently, run in different environments (client, server, and native), and are easy to test. 

 Redux has no relation to React. You can write Redux apps with React, Angular, Ember, jQuery, or vanilla JavaScript

---
#### Document for redux

Before you start coding, you need to be well versed with concepts of Redux. You need to spend enough time to understand the core logic behind redux. The following documentation are official Redux documentation.

https://redux.js.org/

---
#### Redux with React Native

Once you learn about the Redux you can learn about binding React bindings for React . The following is the official documentation for React Redux.

https://react-redux.js.org/

---
#### Installing Redux

React Redux is the official React binding for Redux.

The following link will guide you on installing React Binding for Redux

https://react-redux.js.org/introduction/quick-start

---
#### Initializing Redux

We use the provider tag,<Provider />  to makes the Redux store

https://react-redux.js.org/api/provider

https://redux.js.org/api/store

The connect() function connects a React component to a Redux store.

https://react-redux.js.org/api/connect

---
#### WayPoint 1: Convert ReactNative Basic app to Redux

You have to convert the previous ReactNative project ReactNativeBasic App which you had done before into a Redux app. You have to convert all its functions and work flow in accordance with Redux concepts.

---
#### WayPoint 2: Convert IntekWeather app to Redux

You have to convert the previous ReactNative project IntekWeather App project which you had done before into a Redux app. You have to convert the components into Redux only if you find them to be efficient when compared with pure ReachNative.


---
## Installation instruction

---

## Để có thể hiểu về Redux, cần phải nắm rõ các khái niệm cơ bản sau:
#### 1. Store
#### 2. Actions
#### 3. Reducers
#### 4. Store
---
### 1. Store:


---
### 2. Actions:
Actions là một khối thông tin (thể hiện dưới dạng JavaScript object - giống như dictionary trong Python) mô tả một hành động gửi dữ liệu (data) từ application tới store. 

Điểm đặc biệt của actions là chỉ có duy nhất nó mới có thể được gửi đến store.

Theo document thì ta có thể gửi actions thông qua hàm: store.dispatch()

Action thường là plain JavaScript object và bắt buộc phải có thuộc tính **type**
Giá trị của **type** thường là một chuỗi (strings) mô tả hành động được thực hiện

Giá trị còn lại trong action thường là dữ liệu mà ta muốn gửi đến store (cập nhật hoặc thay đổi). Dưới đây là một ví dụ về một action:
```
const ADD_TODO = 'ADD_TODO'
{
    type: ADD_TODO,
    text: 'Build my first Redux app'
}
```
Ở ví dụ trên, ta vừa tạo ra một Action là một plain JavaScript object với thuộc tính **type** = 'ADD_TODO' và thuộc tính **text** = 'Build my first Redux app'.
Thuộc tính *text* ở đây chính là dữ liệu mà ta muốn gửi đến store để cập nhật hoặc thay đổi.
Ví dụ như trong store cũng có thuộc tính **text** = undefined (rỗng), khi ta dispatch action trên, lúc này thuộc tính **text** trong store sẽ thay đổi, store.**text** = 'Build my first Redux app'.