# CS169 Week3 Section
A basic tutorial of Sinatra.

### Requirements
This tutorial assumes that you are using the Cloud9 IDE.

Find a partner and begin typing the following exercises. You should alternate who types and who explains the output.

#### Install the Sinatra Gem
Type the following command in the C9 terminal:
```
gem install sinatra
```
#### Write a Hello World Sinatra App
Create an empty Ruby workspace. In the root directory of your workspace, create a file ```app.rb```. Type the following content in the file:
```ruby
require "sinatra"

get "/" do
    "Hello, world!"
end
```
#### Start the App
Type the following command in C9 terminal:  
**Note:** Type the following content literally, do not replace anything.
```
ruby app.rb -p $PORT -o $IP
```
#### Try Your App
In your browser, type the following URL to try your first Sinatra app:
```
http://<project-name>.<username>.c9.io
```
Replace ```<project-name>``` and ```<username>``` with your C9 root directory name and your C9 username respectively. For example, my url is:  ```https://test-sinatra-jacksongl.c9users.io/```.

#### Exercise:
Add another page to your site with URL ```http://<project-name>.<username>.c9.io/about```.
The page should display content: ```My name is <your name>.```