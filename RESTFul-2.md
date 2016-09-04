# Basic Sinatra RESTful API

Find a partner and begin typing the following exercises. You should alternate who types and who explains the output.

#### Work out a POST example in Sinatra
Add the following code snippet to ```app.rb`` file:
```ruby
get '/form' do
    erb :form
end

post '/form' do
    "You said #{params[:message]}"
end
```

Create a directory called ```views``` and add a new file called ```form.erb``` with the following content
```html
<form action="/form" method="post">
    <input type="text" name="message">
    <input type="submit">
</form>
```

#### Restart the App
Type <kbd>CTRL</kbd>+<kbd>C</kbd> to terminal the running Sinatra app; and type the following command in C9 terminal to restart it:  
**Note:** Type the following content literally, do not replace anything.
```
ruby app.rb -p $PORT -o $IP
```
#### Try Your App
First go to the following URL:
```
http://<project-name>-<username>.c9users.io/form
```
Type a message in the text box and click <kbd>submit</kbd>. Try to explain how it works.


#### Add a 404 page
Add the following code snippet to ```app.rb``` file:
```ruby
not_found do
  status 404
  'not found'
end
```
Any undefined action will be redirected to the block you passed to ```not_found``` function.

#### Great Resources:
[Singing with Sinatra - The Recall App](http://code.tutsplus.com/tutorials/singing-with-sinatra-the-recall-app--net-19128)
