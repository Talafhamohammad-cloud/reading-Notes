# Django Settings Best Practices:
Different environments. Usually, you have several environments: local, dev, ci, qa, staging, production, etc. Each environment can have its own specific settings (for example: DEBUG = True, more verbose logging, additional apps, some mocked data, etc). You need an approach that allows you to keep all these Django setting configurations.
Sensitive data. You have SECRET_KEY in each Django project. On top of this there can be DB passwords and tokens for third-party APIs like Amazon or Twitter. This data cannot be stored in VCS.
Sharing settings between team members. You need a general approach to eliminate human error when working with the settings. For example, a developer may add a third-party app or some API integration and fail to add specific settings. On large (or even mid-size) projects, this can cause real issues.
Django settings are a Python code. This is a curse and a blessing at the same time. It gives you a lot of flexibility, but can also be a problem – instead of key-value pairs, settings.py can have a very tricky logic.

## Setting Configuration: Different Approaches
There is no built-in universal way to configure Django settings without hardcoding them. But books, open-source and work projects provide a lot of recommendations and approaches on how to do it best. Let’s take a brief look at the most popular ones to examine their weaknesses and strengths.
settings_local.py
This is the oldest method. I used it when I was configuring a Django project on a production server for the first time. I saw a lot of people use it back in the day, and I still see it now.
The Django settings file is a Python code, so settings_local.py can have some non-obvious logic. You need to have settings_local.example (in VCS) to share the default configurations for developers.
Separate settings file for each environment This is an extension of the previous approach. It allows you to keep all configurations in VCS and to share default settings between developers.
## 12 Factors is a collection of recommendations on how to build distributed web-apps that will be easy to deploy and scale in the Cloud. It was created by Heroku, a well-known Cloud hosting provider. The collection consists of twelve parts:
Codebase
Dependencies
Config
Backing services
Build, release, run
Processes
Port binding
Concurrency
Disposability
Dev/prod parity
Logs
***Admin processes Each point describes a recommended way to implement a specific aspect of the project. Some of these points are covered by instruments like Django, Python, pip. Some are covered by design patterns or the infrastructure setup. In the context of this article, we are interested in one part: the Configuration. The Settings file is a small but very important part of any Django project. If you do it wrong, you’ll have a lot of issues during all phases of development. But if you do it right, it will be a good basis for your project that will allow it to grow and scale in the future. Using the environment variables approach, you can easily switch from a monolith to microservice architecture, wrap your project in Docker containers, and deploy it in any VPS or Cloud hosting platform such as: Amazon, Google Cloud, or your own Kubernetes cluster***

## SSH:
SSH, or Secure Shell, is a remote administration protocol that allows users to control and modify their remote servers over the Internet. The service was created as a secure replacement for the unencrypted Telnet and uses cryptographic techniques to ensure that all communication to and from the remote server happens in an encrypted manner. It provides a mechanism for authenticating a remote user, transferring inputs from the client to the host, and relaying the output back to the client.

## Understanding Different Encryption Techniques:
**The significant advantage offered by SSH over its predecessors is the use of encryption to ensure secure transfer of information between the host and the client. Host refers to the remote server you are trying to access, while the client is the computer you are using to access the host. There are three different encryption technologies used by SSH:**
***Symmetrical encryption***
***Asymmetrical encryption***
***Hashing.***
## Symmetric Encryption:
#### Symmetric encryption is a form of encryption where a secret key is used for both encryption and decryption of a message by both the client and the host. Effectively, any one possessing the key can decrypt the message being transferred.

## Asymmetric Encryption
### Unlike symmetrical encryption, asymmetrical encryption uses two separate keys for encryption and decryption. These two keys are known as the public key and the private key. Together, both these keys form a public-private key pair.
## Hashing:
### One-way hashing is another form of cryptography used in Secure Shell Connections. One-way-hash functions differ from the above two forms of encryption in the sense that they are never meant to be decrypted. They generate a unique value of a fixed length for each input that shows no clear trend which can exploited. This makes them practically impossible to reverse.