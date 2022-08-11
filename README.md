_English | [Chinese](./README.zh.md)_

Update time: 2022-08-11

# react-native-chat-sdk

Instant messaging connects people wherever they are and allows them to communicate with others in real time. The Agora Chat SDK enables you to embed real-time messaging in any app, on any device, anywhere.

## Directory description

├── CHANGELOG.md // Release notes document  
├── CONTRIBUTING.md // Contributor documentation  
├── LICENSE // License file  
├── README.md // Project help documentation  
├── README.zh.md // Project help documentation (Chinese version)  
├── android // react native SDK android platform folder  
├── docs // docs folder  
├── example // project built-in demo  
├── examples // Independent demo outside the project  
├── ios // react native SDK ios platform folder  
├── lib // react native SDK generates product folder  
├── native_src // react native SDK native source code folder  
├── node_modules // react native depends folder, generated by `yarn` or `npm` command  
├── package.json // react native project management file  
├── scripts // react native script folder  
├── src // react native source code folder  
├── tsconfig.build.json // typescript language build configuration file  
├── tsconfig.json // typescript language configuration file  
└── yarn.lock // yarn project dependency version configuration file

## Project development environment requirements

The requirements are as follows:

- React Native 0.63.4 or above
- NodeJs 16 or above
- Xcode 12.4 or above for iOS application
- Android Studio 4.2 or above for Android application

For details, please refer to the Quick Start demo. [Portal](./docs/quick-start.md)

## Add SDK to existing application

Open the terminal and go to the existing project folder to add SDK dependencies:

```sh
yarn add react-native-chat-sdk
```

or

```sh
npm i --save react-native-chat-sdk
```

## General Usage

### Initialization SDK

```typescript
ChatClient.getInstance()
  .init(
    new ChatOptions({
      appKey: '<your app key>',
    })
  )
  .then(() => {
    console.log('init success');
  })
  .catch((reason) => {
    console.log('init fail:', reason);
  });
```

### Login

```typescript
ChatClient.getInstance()
  .loginWithAgoraToken('<your account ID>', '<your token>')
  .then((value: any) => {
    console.log(`login success`, value);
  })
  .catch((reason: any) => {
    console.log(`login fail:`, reason);
  });
```

### Others

Please refer to the corresponding example or method description.

## quick start

See the Quick Start documentation for details. [Portal](./docs/quick-start.md)

## demo experience

For details, see the demo of running the experience api. [portal](./example/package.json).
For details, see the demo of running experience login, logout, sending and receiving messages. [portal](./examples/simple_demo/package.json).

## Contributors

See Contributor Guide for details. [Portal](./CONTRIBUTING.md).

## Release Notes

See the changelog for details. [Portal](./CHANGELOG.md).

## Release type description

See version type description for details. [Portal](./docs/version-types.md).

## Developer Instructions

See developer instructions for details. [Portal](./docs/developer.md).

## User Instructions

See the User Instructions [Portal](./docs/user.md) for details.

## License

MIT

## Q & A

If you encounter problems, please refer to here. [Portal](./docs/others.md).

## References

[Github repository address](https://github.com/easemob/react-native-chat-sdk)
[Official website document address](https://docs-im.easemob.com/ccim/rn/quickstart)
