# [RingCentral Embeddable](https://ringcentral.github.io/ringcentral-embeddable/)

[![Build Status](https://github.com/ringcentral/ringcentral-embeddable/workflows/CI%20Pipeline/badge.svg?branch=master)](https://github.com/ringcentral/ringcentral-embeddable/actions)

## Introduction

This is an out-of-the-box embeddable web application that help developers to integrate RingCentral services to their web applications with few code.

Built with:

* [RingCentral Widgets](https://github.com/ringcentral/ringcentral-js-widgets) - based on React and Redux

## Visit Online

Visit [website](https://ringcentral.github.io/ringcentral-embeddable/) in GitHub Pages.

## Use as a embeddable web widget

### Get Started

there are two ways to integrate this widget to a web application

#### Adapter JS way

Just add following code to a website's header. It will create a RingCentral Embeddable widget in that web page.

```js
<script>
  (function() {
    var rcs = document.createElement("script");
    rcs.src = "https://ringcentral.github.io/ringcentral-embeddable/adapter.js";
    var rcs0 = document.getElementsByTagName("script")[0];
    rcs0.parentNode.insertBefore(rcs, rcs0);
  })();
</script>
```

#### Iframe way

Create a iframe with the following code:

```html
<iframe width="300" height="500" id="rc-widget" allow="autoplay; microphone" src="https://ringcentral.github.io/ringcentral-embeddable/app.html">
</iframe>
```

You can use the config tool in this [page](https://ringcentral.github.io/ringcentral-embeddable) to generate code with config.

#### Stable version

We provide latest RingCentral Embeddable version on github page `https://ringcentral.github.io/ringcentral-embeddable`. It includes latest features and bugfix in RingCentral Embeddable. And it will keep up to date with master code. But we **recommend** developers to use versioned RingCentral Embeddable. You can get current latest stable version of RingCentral Embeddable from [here](https://github.com/ringcentral/ringcentral-embeddable/releases). Such as `1.4.1`, you can get versioned app in this uri `https://apps.ringcentral.com/integration/ringcentral-embeddable/1.4.1`.

Just replace `https://ringcentral.github.io/ringcentral-embeddable` in [upper code](#adapter-js-way) to the versioned uri, and you will be using versioned RingCentral Embeddable. The versioned app will not be influenced when new features are added, so it will be more stable than latest version. When you need to update RingCentral Embeddable, you need to update the versioned app uri in your code manually.

For stable version from `1.0.2`, it is required to setup your own RingCentral client id. Please follow [here](docs/config-client-id-and-secret.md) to setup, or it will throw error with client id required.
For stable version from `1.2.0`, authorization redirect uri will change with version as `https://apps.ringcentral.com/integration/ringcentral-embeddable/1.4.1/redirect.html`, but you can make a fixed redirect URI with this [docs](docs/customize-redirect-uri.md).

To get all versions of RingCentral Embeddable in [here](https://github.com/ringcentral/ringcentral-embeddable/releases).

### Documents

* [Get Started](docs/get-started.md)
* [Browser Support](docs/browser-support.md)
* [Use your own app client id](docs/config-client-id-and-secret.md)
* [Customize Redirect Uri](docs/customize-redirect-uri.md)
* [Enable Multiple Tabs Support](docs/multiple-tabs.md)
* [Multiple Partner Brands Support](docs/multiple-brands.md)
* [Customize prefix](docs/customize-prefix.md)
* [Work with the Web Widget event](docs/widget-event.md)
  * [Web phone call event](docs/widget-event.md#web-phone-call-event)
  * [Ringout call event](docs/widget-event.md#ringout-call-event)
  * [Active Call event](docs/widget-event.md#active-call-event)
  * [Login Status event](docs/widget-event.md#login-status-event)
  * [Message event](docs/widget-event.md#message-event)
  * [Route event](docs/widget-event.md#route-changed-event)
* [API to control the Web Widget](docs/control-widget.md)
  * [Go to Dial and start a call](docs/control-widget.md#go-to-dial-and-start-a-call)
  * [Go to SMS](docs/control-widget.md#go-to-sms-page)
  * [Control the web call](docs/control-widget.md#control-the-web-call)
    * Answer a ringing call
    * Reject a ringing call
    * Hangup a call
  * [Log out user](docs/control-widget.md#log-out-user)
  * [Minimize and Hide widget](docs/control-widget.md#minimizehideremove-the-widget)
  * [Navigate to](docs/control-widget.md#navigate-to)
  * [Schedule a meeting (RingCentral Video/RingCentral Meetings)](docs/control-widget.md#schedule-a-meeting)
* [Work with RingCentral C2D](docs/work-with-ringcentral-c2d.md)
* [Interact with calling settings](docs/interact-with-calling-settings.md)
* [Third Party Service in Widget](docs/third-party-service-in-widget.md)
  * Register your service
  * Add meeting schedule button with your service
  * Show upcoming meeting list in RingCentral Video page
  * Log RingCentral Video meeting into your service
  * Show contacts from your application
  * Show contact's activities from your application
  * [Log call into your service](docs/third-party-service-in-widget.md#log-call-into-your-service)
  * [Log messages into your service](docs/third-party-service-in-widget.md#log-messages-into-your-service)
  * Add third party authorization button
  * [Third Party Settings](docs/third-party-service-in-widget.md#third-party-settings)
* [Enable and Disable Features in Widget](docs/disable-features.md)
  * Disable messages features
  * Disable Call releated features
  * Enable Conference invite feature
  * [Enable Glip feature](docs/disable-features.md#enable-glip-feature)
  * [Enable Conference(3-way) Calling feature](docs/disable-features.md#enable-conference-call-feature)
  * [Enable Active Call Control feature](docs/disable-features.md#enable-active-call-control-feature)
* [New adapter badge UI](docs/new-adapter-ui.md)
* [Enable Analytics](docs/add-analytics.md)
* [Customize Widget UI styles](docs/customize-ui-styles.md)
* [Popup a standalone widget](docs/popup-window.md)
## Awesome Embeddable projects

* RingCentral Embeddable phone for Hubspot CRM - [repo](https://github.com/ringcentral/hubspot-embeddable-ringcentral-phone)
* RingCentral Embeddable phone for Insightly CRM- [repo](https://github.com/ringcentral/insightly-embeddable-ringcentral-phone)
* RingCentral Embeddable phone for Pipedrive CRM - [repo](https://github.com/ringcentral/pipedrive-embeddable-ringcentral-phone-spa)
* RingCentral Embeddable with Salesforce Lightning - [tutorial](https://ringcentral-web-widget-demos.readthedocs.io/en/latest/salesforce_lightning/tutorial/)
* RingCentral Embeddable with Static CRM - [tutorial](https://ringcentral-web-widget-demos.readthedocs.io/en/latest/static_crm/tutorial/)
* RingCentral Embeddable with chrome extension - [repo](https://github.com/embbnux/ringcentral-embeddable-voice-extension)
* Ringcentral Embeddable for Google with Firefox add-on - [repo](https://github.com/embbnux/ringcentral-embeddable-for-google-firefox-addon)
* RingCentral Embeddable with Third Party service - [repo](https://github.com/embbnux/ringcentral-embeddable-voice-with-third-party)
* RingCentral Embeddable with Electron - Support Linux - [repo](https://github.com/embbnux/ringcentral-embeddable-voice-app)
* RingCentral Embeddable with Game of Thrones theme - [repo](https://github.com/embbnux/ringcentral-web-widget-styles)
* RingCentral Embeddable with Java app - jxBrowser - [repo](https://github.com/tylerlong/jxbrowser-webrtc)
* RingCentral Embeddable extension factory - Extension CLI build tool - [repo](https://github.com/ringcentral/ringcentral-embeddable-extension-factory)

## Contribution and Development

We provide a online version that developers can use to embed and config in their web application. When you want to get a deep development of this widget, you can clone code of this widget, update it and deploy by yourself.

### Clone the code

```bash
$ git clone https://github.com/ringcentral/ringcentral-embeddable.git
```

### Create a free RingCentral app

1. Create a [RingCentral developer free account](https://developer.ringcentral.com)
2. Create a RingCentral app with platform type - "Browser Based"
3. Add permissions `Edit Message`, `Edit Presence`, `Internal Messages`, `Read Accounts`, `Read Call Log`, `Read Contacts`, `Read Messages`, `Read Presence`, `RingOut`, `SMS`, `Glip`, `VoIP Calling` and `Call Control` to your app.
4. Add redirect uri `http://localhost:8080/redirect.html` to your app settings.

### Create environment variables file in project root path

Create `.env` file in project root path:

```
API_KEY=your_ringcentral_app_client_id
API_SERVER=ringcentral sever url, eg: https://platform.devtest.ringcentral.com
TEST_HOST_URI=http://localhost:8080
TEST_USER_NAME=your_sandbox_account_phone_number
TEST_USER_PASSWORD=your_sandbox_account_password
TEST_HEADLESS=false
```

`TEST_*` variables is optional for automatic test, you can just keep it blank before you run automatic tests.

### Start development server

We assume you have pre-installed node.js > 8 and yarn.

**It is recommended to use `yarn` instead of `npm`.** We have `yarn.lock` file in source code to lock dependence version. With `yarn`, we can install dependencies with correct version that work well with this project.

```bash
$ yarn       # use yarn to install dependences
$ yarn start # start a webpack dev server
```

Open site: 'http://localhost:8080/' on browser

### Run Tests

You need to update `.env` file to add environment variables for test as mentioned in previous section.

```
yarn test
```

### Deploy on production

If you create pull request to this repo and get merged, CI will deploy it to this repository's Github Page automatically. But for something that customized, you can deploy it to your own web space, such as your github page.

1. Update `.env` file in production environment ([Graduate your RingCentral app to get production app client id](docs/config-client-id-and-secret.md#graduation-for-your-ringcentral-app))

2. Run command to compile code and build release

```
$ HOSTING_URL=your_host_uri
```

Please replace `your_host_uri` with your own web host address, such as `https://ringcentral.github.io/ringcentral-embeddable`.

And set redirect uri `${your_host_uri}/redirect.html` in your app setting on RingCentral Developer website.

3. Upload all files in release folder to your web space. And visit it in browser.

### Build for browser extension

For browser extension, we can host all files in browser extension local folder instead CDN.

To build for browser extension local files:

```
yarn build-extension
```

After building, we can get compiled files in this project's extension folder. Create a `embeddable` folder in your extension project. Copy all files in extension folder to your extesnion project's `embeddable` folder.

Then you can load this widget with `${your_extension_uri}/embeddable/adapter.js` or `${your_extension_uri}/embeddable/app.html`.
