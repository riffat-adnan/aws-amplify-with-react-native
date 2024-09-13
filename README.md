# AWS Amplify with React Native

This repository demonstrates how to integrate AWS Amplify into a React Native project to enable features such as authentication, storage, APIs, and more. AWS Amplify simplifies the development of serverless applications, allowing you to build cloud-powered apps quickly and securely.

## Table of Contents

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Running the App](#running-the-app)
- [Amplify CLI Commands](#amplify-cli-commands)
- [Screens](#screens)
- [Built With](#built-with)
- [Contributing](#contributing)
- [License](#license)

## Features

- AWS Cognito for authentication (sign-in, sign-up, reset password)
- AWS S3 for file storage (upload and download files)
- GraphQL API with AWS AppSync
- Real-time data and subscriptions with GraphQL
- Integration with Amplify CLI for deployment
- Secure environment management with Amplify

## Prerequisites

Before you begin, make sure you have the following installed:

- **Node.js** (v14 or higher)
- **React Native CLI** or **Expo CLI**
- **AWS Amplify CLI** installed globally:
  ```bash
  npm install -g @aws-amplify/cli
  ```
- **AWS Account** to configure Amplify resources

## Installation

### 1. Clone the repository:
```bash
git clone https://github.com/ali-zeee/aws-amplify-with-react-native.git
cd aws-amplify-with-react-native
```

### 2. Install dependencies:
```bash
npm install
# or
yarn install
```

### 3. Initialize Amplify:
```bash
amplify init
```
- Follow the prompts to configure Amplify for your project. Select default options unless you have specific preferences.

### 4. Add Amplify Authentication:
```bash
amplify add auth
```
- Configure authentication based on your requirements (default settings provide user sign-up/sign-in).

### 5. Add an API (optional):
```bash
amplify add api
```
- Select **GraphQL** to create an AppSync API, or choose **REST API** if needed.

### 6. Deploy Amplify resources to AWS:
```bash
amplify push
```

## Configuration

1. After setting up Amplify and deploying resources, the `aws-exports.js` file will be generated in your project.
2. You can now use the Amplify SDK to interact with the AWS services (e.g., authentication, API calls, storage).
3. Example code to configure Amplify:
   ```javascript
   import Amplify from 'aws-amplify';
   import awsconfig from './aws-exports';

   Amplify.configure(awsconfig);
   ```

## Running the App

### iOS
```bash
npx react-native run-ios
```

### Android
```bash
npx react-native run-android
```

### Using Expo (if applicable)
```bash
expo start
```

## Amplify CLI Commands

Here are some of the common AWS Amplify CLI commands:

- `amplify init` – Initializes a new Amplify project.
- `amplify add auth` – Adds authentication to the app (Cognito).
- `amplify add api` – Adds a GraphQL or REST API.
- `amplify push` – Deploys your resources to the cloud.
- `amplify status` – Displays the status of your local resources.
- `amplify publish` – Publishes your app and backend to the cloud.

For more details, refer to the [Amplify CLI documentation](https://docs.amplify.aws/cli).

## Built With

- **React Native** - Cross-platform framework for mobile app development.
- **AWS Amplify** - Framework for developing and deploying cloud-powered mobile applications.
- **AWS Cognito** - Secure user authentication and access control.
- **AWS AppSync** - Managed GraphQL service for real-time data queries and subscriptions.
- **AWS S3** - Scalable storage service for storing and retrieving files.

## Contributing

Contributions are welcome! If you'd like to contribute to this project, please follow these steps:

1. Fork the repository.
2. Create a feature branch: `git checkout -b my-feature`.
3. Commit your changes: `git commit -m 'Add new feature'`.
4. Push to the branch: `git push origin my-feature`.
5. Open a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
```

This `README.md` provides detailed information on the project setup, including installation steps, AWS Amplify integration, and key features. Feel free to replace the URLs for screenshots and make any necessary adjustments for your specific use case.