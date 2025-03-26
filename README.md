# Instagram Automation Bot

This is an Instagram bot built using `instabot` that allows users to automate various Instagram actions such as:
- Logging into an account
- Following users
- Uploading photos with captions
- Unfollowing users
- Sending messages to users
- Fetching followers and following lists

## Features
- **Follow Users:** Automatically follow specific users.
- **Upload Photos:** Post images with captions.
- **Unfollow Users:** Remove specific users from your following list.
- **Send Messages:** Send direct messages to one or multiple users.
- **Get Followers List:** Retrieve and display a list of followers.
- **Get Following List:** Retrieve and display a list of users you are following.

## Installation
Ensure you have Python installed on your system, then install the required library:
```sh
pip install instabot
```

## Usage
Create a Python script with the following code and update the `username` and `password` fields with your Instagram credentials:

```python
from instabot import Bot

bot = Bot()
bot.login(username="your_username", password="your_password")

# Follow a user
# bot.follow("instagram_username")

# Upload a photo
# bot.upload_photo("path/to/image.jpg", caption="Your caption here")

# Unfollow a user
# bot.unfollow("instagram_username")

# Send a direct message
# bot.send_message("Hello!", ["username1", "username2"])

# Get list of followers
# followers = bot.get_user_followers("your_username")
# for follower in followers:
#     print(bot.get_user_info(follower))

# Get list of users you are following
following = bot.get_user_following("your_username")
for user in following:
    print(bot.get_user_info(user))
```

