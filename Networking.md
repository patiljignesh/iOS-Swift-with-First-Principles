# Networking

## Step 1 : Creating a URL

## Step 2: Create a URLSession
- Its same as enabeling a session in the browser after entering the url with the default settings

## Step 3: Give URLSession a task
- Creates a task that retrieves the contents of the specified URL, then calls a handler upon completion.
## Step 4: Start a task
- Newly-initialized tasks begin in a suspended state, so you need to call this method to start the task.

```
task.resume()

````
