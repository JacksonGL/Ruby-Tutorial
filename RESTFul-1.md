# Basic Sinatra RESTful API

Find a partner and begin typing the following exercises. You should alternate who types and who explains the output.

#### Get Single Parameter from URL
add the following code snippet to ```app.rb`` file:
```ruby
get "/getname/:name" do |name|
    "Welcome, #{params[:name]}!"
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
http://<project-name>-<username>.c9users.io/getname/<your name>
```
Try to explain what happended.


#### Get Multiple Parameters from URL
add the following code snippet to ```app.rb```:
```ruby
get '/getname/:name/:city' do
  "Hey there #{params[:name]} from #{params[:city]}."
end
```
In your browser, type the following URL:
```
http://<project-name>-<username>.c9users.io/getname/<your name>/<your city>
```
Try to explain what happended.

#### Duplicated Routing
add the following code snippet to ```app.rb``` (right after the above code snippet)
```ruby
get '/getname/:name/:city' do
  "Alternative routing result: #{params[:name]} from #{params[:city]}."
end
```
Restart the server, in your browser, type the following URL:
```
http://<project-name>-<username>.c9users.io/getname/<your name>/<your city>
```
See the result in the browser and reorganize your code to change the code snippet order as follows:
```ruby
get '/getname/:name/:city' do
  "Alternative routing result: #{params[:name]} from #{params[:city]}."
end

get '/getname/:name/:city' do
  "Hey there #{params[:name]} from #{params[:city]}."
end
```
Try to explain what happended.

#### Next
add the following code snippet to the end of ```app.rb```:
```ruby
get '/getname/*' do
    arr = params[:splat]
    ret = ''
    arr[0].split('/').each do |param| 
        ret += (param + '<br/>')
    end
    ret
end
```
In your browser, type the following URL:
```
http://<project-name>-<username>.c9users.io/getname/1/2/3/4
```
Try to explain what happended.


Go to the [next page](RESTFul-2.md) of this Tutorial

