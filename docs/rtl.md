# RTL Support

BootstrapVue does not have RTL support, but it is possible to add RTL support to your Builderall Vue Ui application just by 
inserting the document direction in the `html` tag and informing if you want your application to behave in RTL when using the library (you can use the `dir` attribute itself for that)

`index.html`
```html
<html dir="rtl">
<html dir="ltr">
```

`app.js`
```js
Vue.use(BuilderallVueUi, {
	rtl: document.documentElement.dir == 'rtl'
})
```
_________

**Note:** This library offers RTL support only to its own components and to Bootstrap vue components with custom CSS. To customize other things, you can add necessary CSS within the selector `html[dir=rtl]`
