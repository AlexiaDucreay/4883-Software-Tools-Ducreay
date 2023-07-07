## Assignment 6 - Software Tool Presentation

#### Due: Multiple Dates

### Understanding SendBird

SendBird is a leading communication platform that offers APIs and SDKs to integrate real-time messaging and chat functionalities into web and mobile applications. It provides developers with a robust infrastructure, simplifying the complex process of implementing real-time communication features from scratch.

# SendBird

## Introduction

SendBird is a powerful cloud-based chat and messaging platform that allows developers to integrate real-time chat functionality into their applications. It provides a comprehensive set of features and tools that enable the building of interactive and scalable chat experiences across various platforms, including web, mobile, and desktop.

This README provides an overview of the features offered by SendBird, explains how it works, and provides guidance on implementing SendBird into your application with example code.

## Features

SendBird offers a wide range of features to enhance your chat application:

- Real-Time Messaging
- Group Channels
- User Management
- Push Notifications
- Typing Indicators
- Read Receipts
- File and Image Uploads
- Moderation and Profanity Filter

These features are just a glimpse of what SendBird has to offer.

## How SendBird Works

SendBird operates on a client-server architecture, where clients (web, mobile, desktop, etc.) interact with the SendBird server to send and receive messages. The SendBird server handles the storage and delivery of messages between clients, ensuring real-time communication.

The key components and workflow in SendBird are as follows:

1. **Users**: Users are the participants in a chat application. Each user is identified by a unique user ID and can have additional profile information.

2. **Channels**: Channels are virtual spaces where users can exchange messages. SendBird supports various types of channels, such as open channels (public chat rooms) and group channels (private chat rooms).

3. **Messages**: Messages are the units of communication in SendBird. They can contain text, multimedia attachments, or custom data. Messages are sent and received in real-time between users.

4. **SendBird Server**: The SendBird server handles the authentication, message storage, and delivery. It acts as a relay between clients, ensuring messages reach their intended recipients.

5. **APIs**: SendBird provides RESTful APIs and SDKs that developers can use to interact with the SendBird server. The APIs enable operations such as creating channels, sending messages, managing users, and more.

## Getting Started

To start using SendBird in your application, follow these steps:

1. Sign up for SendBird: Sign up for a SendBird account at https://dashboard.sendbird.com/auth/signup and create a new application to obtain an App ID.

2. Install SendBird SDK: Depending on your platform, install the SendBird SDK that corresponds to your application. SendBird offers SDKs for various platforms, including iOS, Android, JavaScript, Unity, and more. Visit the [SendBird documentation](https://docs.sendbird.com/) for detailed installation instructions.

3. Initialize SendBird: Before you can use SendBird in your application, initialize it with your App ID. This step authenticates your application with SendBird and allows you to establish a connection with the server. Here's an example of initializing SendBird in JavaScript:
   ```javascript
   import * as SendBird from 'sendbird';

   const APP_ID = 'YOUR_APP_ID';
   SendBird.init(APP_ID);

Replace **'YOUR_APP_ID'** with the actual App ID obtained from the SendBird dashboard.  

#### Image:
![IMG_20180110_001701_281]("C:\Users\alexi\Pictures\SendBird\Application ID.png")

User Authentication: To interact with SendBird, you need to authenticate your users. Use the SendBird SDK to authenticate a user and obtain a user token. Here's an example in JavaScript:

```javascript
const USER_ID = 'YOUR_USER_ID';
const USER_NICKNAME = 'John Doe';

SendBird.login({ userId: USER_ID, nickname: USER_NICKNAME }, (user, error) => {
  if (error) {
    console.error(error);
    return;
  }
  // User authentication successful
});


