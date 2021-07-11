# UIViewController and its Lifecyle

## Step 1 - viewDidLoad()
> All the view related objects get connected up and accessible 
> Only called once the view has been created
## Step 2 - viewWillAppear()
> Called just before view about to be visible to the users
> User are not able to see anything yet but it allows us to manipulate(hide/show) elements before the user sees the view 
## Step 3 - ViewDidAppear()
> This is when the users are able to see elements on the screen
> View is visible and anything that needs to be visible to the users on the screen should be executed here
## Step 4 - ViewWillDisappear()
> This is when the user interacts with the screen and ready to navigate away from the screen
> Great time to perform changes before user has been navigated away
## Step 5 - ViewDidDisappear()
> This stage, view has disappeared and not visible to the user
> Last moment to make changes to the previous view before the next view is loaded to the user
