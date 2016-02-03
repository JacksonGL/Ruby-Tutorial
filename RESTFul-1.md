# Basic Sinatra RESTful API

Find a partner and begin typing the following exercises. You should alternate who types and who explains the output.

#### Get Single Parameter from URL
add the following code snippet to ```app.rb`` file:
```
get "/getname/:name" do
    "Welcom, #{params[:name]}!"
end
```
#### Restart the App
Type <kbd>CTRL</kbd>+<kbd>C</kbd> to terminal the running Sinatra app; and type the following command in C9 terminal to restart it:  
**Note:** Type the following content literally, do not replace anything.
```
ruby app.rb -p $PORT -o $IP
```
#### Try Your App
In your browser, type the following URL:
```
http://<project-name>.<username>.c9.io/getname/<your name>
```
Try to explain what happended.


#### Get Multiple Parameters from URL
add the following code snippet to ```app.rb```:
```
get '/getname/:name/:city' do
  "Hey there #{params[:name]} from #{params[:city]}."
end
```
In your browser, type the following URL:
```
http://<project-name>.<username>.c9.io/getname/<your name>/<your city>
```
Try to explain what happended.