# Basic Sinatra RESTful API

Find a partner and begin typing the following exercises. You should alternate who types and who explains the output.

#### Work out a POST example in Sinatra
add the following code snippet to ```app.rb`` file:
```
get '/form' do
    erb :form
end

post '/form' do
    "You said #{params[:message]}"
end
```

Create a directory called ```views``` and add a new file called ```form.erb``` with the following content
```
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
http://<project-name>.<username>.c9.io/form
```
Type a message in the text box and click <kbd>submit</kbd>. Try to explain how it works.



