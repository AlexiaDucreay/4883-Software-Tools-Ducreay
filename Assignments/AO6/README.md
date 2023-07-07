## Assignment 6 - Software Tool Presentation
## Topic: SendBird
### Name: Alexia Ducreay

![https://www.prweb.com/releases/sendbird_joins_unicorn_club_as_mobile_communications_become_essential_in_the_lives_of_billions_of_people_across_the_globe/prweb17845762.htm)

### Understanding SendBird

SendBird is a leading communication platform that offers APIs and SDKs to integrate real-time messaging and chat functionalities into web and mobile applications. It provides developers with a robust infrastructure, simplifying the complex process of implementing real-time communication features from scratch.

# SendBird

## Introduction

SendBird is a powerful cloud-based chat and messaging platform that allows developers to integrate real-time chat functionality into their applications. It provides a comprehensive set of features and tools that enable the building of interactive and scalable chat experiences across various platforms, including web, mobile, and desktop.

This README provides an overview of the features offered by SendBird, explains how it works, and provides guidance on implementing SendBird into your application with example code.

## languages SendBird Support

- iOS: SendBird offers a native iOS SDK, allowing developers to incorporate real-time chat, messaging, and voice/video calling functionalities into their iOS applications using Swift or 
  Objective-C.

- Android: SendBird provides a native Android SDK, enabling developers to integrate real-time communication features into their Android applications using Java or Kotlin.

- JavaScript: SendBird supports JavaScript, providing a JavaScript SDK that can be used to integrate real-time chat and messaging capabilities into web applications or hybrid mobile 
  applications using frameworks like React or Angular.

- React Native: SendBird offers a React Native SDK, allowing developers to build cross-platform mobile applications with real-time chat functionalities using JavaScript.

- Unity: SendBird provides a Unity SDK, enabling developers to integrate real-time chat and messaging features into Unity-powered games and applications.

- .NET: SendBird offers a .NET SDK, allowing developers to incorporate real-time chat functionalities into their applications developed using .NET frameworks, such as ASP.NET or Xamarin.

## Integrations

- SendBird offers integrations with various popular tools and platforms to enhance the functionality and capabilities of its real-time communication platform. Here are some notable SendBird integrations:

- Firebase: SendBird integrates seamlessly with Firebase, a comprehensive mobile development platform provided by Google. By combining SendBird with Firebase, you can leverage Firebase's 
  authentication, real-time database, and cloud functions to enhance your chat application's functionality and security.

- Twilio: Twilio integration allows you to enhance your real-time communication capabilities by leveraging Twilio's robust SMS and voice calling services. With this integration, you can 
  extend SendBird's chat functionality with SMS notifications and enable voice-calling features within your application.

- React Native: SendBird offers a React Native SDK, enabling developers to build cross-platform mobile applications with real-time chat capabilities. The integration provides native 
  support for both iOS and Android platforms, allowing you to create engaging and interactive chat experiences.

- Zendesk: By integrating SendBird with Zendesk, a leading customer support platform, you can streamline customer service interactions. This integration allows you to escalate chat 
  conversations from SendBird to Zendesk, enabling seamless transition and efficient management of support tickets.

- Salesforce: SendBird's integration with Salesforce brings real-time chat capabilities to the Salesforce platform. This integration enables customer support agents to engage in real-time 
  conversations with customers, enhancing the overall customer experience and improving response times.

- Stripe: SendBird's integration with Stripe, a popular payment processing platform, enables businesses to facilitate secure and seamless in-app purchases. This integration allows you to 
  combine real-time chat with payment functionality, creating a smooth transaction experience for your users.

- Unity: SendBird offers a Unity SDK, enabling developers to integrate real-time chat and messaging capabilities into their Unity-powered games and applications. This integration allows 
  for in-game chat, multiplayer interactions, and community building within the Unity environment.

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

3. **Messages**: Messages are the units of communication in SendBird. They can contain text, multimedia attachments, or custom data. Messages are sent and received in real time between users.

4. **SendBird Server**: The SendBird server handles authentication, message storage, and delivery. It acts as a relay between clients, ensuring messages reach their intended recipients.

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

#### Application ID:
<img width="1004" alt="Application ID" src="https://github.com/AlexiaDucreay/4883-Software-Tools-Ducreay/assets/48137129/67f58325-88d9-4611-a62f-9a7f74e13284">


User Authentication: To interact with SendBird, you need to authenticate your users. Use the SendBird SDK to authenticate a user and obtain a user token. Here's an example in JavaScript:

    ```javascript
    const USER_ID = 'YOUR_USER_ID';
    const USER_NICKNAME = 'John Doe';

  `  SendBird.login({ userId: USER_ID, nickname: USER_NICKNAME }, (user, error) => {
      if (error) {
        console.error(error);
        return;
      }
      // User authentication successful
    });


Replace **'YOUR_USER_ID'**  and **'John Doe'** with the appropriate user information.


Creating and Joining Channels: Once users are authenticated, you can create or join channels to enable chat functionality. Here's an example of creating a group channel in JavaScript:

    ```javascript
    const channelParams = new SendBird.GroupChannelParams()
      .setName('My Group Channel')
      .addUserIds(['USER_ID_1', 'USER_ID_2'])
      .setCoverUrl('https://example.com/channel_cover_image.jpg')
      .setData({ customKey: 'customValue' });

    SendBird.GroupChannel.createChannel(channelParams, (channel, error) => {
      if (error) {
        console.error(error);
        return;
      }
      // Channel created successfully
    });

Replace **'USER_ID_1'** and **'USER_ID_2'** with the user IDs of the participants you want to add to the channel.

<img width="874" alt="Channels" src="https://github.com/AlexiaDucreay/4883-Software-Tools-Ducreay/assets/48137129/6c592ad5-dad0-41b3-9679-83cc5ff9734b">


Sending and Receiving Messages: With channels created, you can send and receive messages between users. Here's an example of sending a message in JavaScript:
    
    ```javascript
    const channelUrl = 'CHANNEL_URL';
    
    const params = new SendBird.UserMessageParams()
      .setMessage('Hello, SendBird!')
      .setCustomType('greeting')
      .setData({ additionalData: 'value' });
    
    SendBird.GroupChannel.getChannel(channelUrl, (channel, error) => {
      if (error) {
        console.error(error);
        return;
      }
    
      channel.sendUserMessage(params, (message, error) => {
        if (error) {
          console.error(error);
          return;
        }
        // Message sent successfully
      });
    });
Replace **'CHANNEL_URL'** with the URL of the desired channel.



