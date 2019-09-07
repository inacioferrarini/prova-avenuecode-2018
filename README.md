# iOS Code Challenge

## MOB-01 - TV Shows screen 

As a user I want to see a list of existent TV Shows. I should be able to **Save** shows as **Favorite** or **Delete** them if they are already saved.

### Acceptance Criteria

- This is the App's first and main screen.
- When screen Loads app should fetch a list of TV shows from the TVMaze API
- Screen **must** have a [larger navigation bar](https://bitbucket.org/ac-recruitment/ios-challenge/src/master/Assets/largeTitle.png) that needs to [shrink as user is scrolling](https://bitbucket.org/ac-recruitment/ios-challenge/src/master/Assets/collapsed.png).
- Screen **must** follow guidelines described [here](https://bitbucket.org/ac-recruitment/ios-challenge/src/master/Assets/largeTitle.png)
- Each item in the Table View is a TV Show, and should show the following properties:
    - Image View with TV Show's poster { `JSON Key: image.medium` }
        - Image needs to be lazyly downloaded
        - Once image is downloaded, it **needs** to be stored locally for later use
    - Label with TV Show's name { `JSON Key: name` }
- Each Row of the TableView **must** have an action to **Delete** or **Favorite** the TV Show
    - When TV Show **is already** saved, show **Delete** action
    - When TV Shows **is not** saved, show **Favorite** action
- **Delete** action must have a Red background and **Delete** as title
- **Favorite** action must have a Green background and **Favorite** as title
- TV Shows saved as favorite need to be accessed offline.
    - You can save as many TV Show's properties as you wish
- When user selects to save a TV Show, you **must** save it in a **Database** of your choosing.
- When deleting a TV Show, a confirmation popup needs to be shown to confirm deletion.
- After deleting, TV Show need to be removed from local database
- When any user action fails, a retry dialog should be shown. The retry dialog should have:
    - Title 
         - Oops, something went wrong
    - Message:
         - For saving/removing favorite: 
            - There was a problem saving/deleting this TV Show. Do you want to try again?
         - For timeout / no connection:
            - An error occurred while fetching data. Do you want to try again?
    - Cancel option
    - Retry option
- When user selects a TV Show the **Details** (MOB-03) screen should be shown.
- App **must** have a TabBar where user can navigate to **TV Shows** (MOB-01) and **Favorites** (MOB-02) screens

## MOB-02 - Favorites Screen

As a user I want to see all the TV Shows I marked as favorites, having the option to delete them from my favorites.

#### Acceptance Criteria

- This screen shows all TV Shows already saved as favorites.
- Each Row of the TableView **must** have an action to **Delete** TV Show.
- When user tries to delete a TV Show, app must show a confirmation popup.
- When user deletes a TV Show from favorites, app **must** remove it from database and update Table View.
- When user taps on a TV Show, **Details** screen (MOB-03) must be shown.

## MOB-03 - Details Screen

As a user I want to see TV Show's details and **add** or **delete** TV Shows to/from favorite list.

### Acceptance Criteria

- This screen should have:
    - Image View with TV Show's poster { `JSON Key: image.original` }
    - Label with TV Show's summary { `JSON Key: summary` }
    - Button linking to Show's IMDb page { `JSON Key: externals.imdb` }
    - Any other information you find revelant
- This screen's design is up to you.
- Navigation Controller's title should be the TV Show's name.
- When there's no IMDb ID, button should be invisible
- A button on the right side of the Navigation Controller should be visible to save or delete the TV Show
    - When TV Show **is already** saved as favorite show a **Delete** button.
    - When TV Show **is not** saved, show a **Favorite**
    - You can customize this button the way you want.


## Technical Details:
- **Language**: **Swift** 
- **Persitence**: Any local database can be used.
- **Architecture**: You can choose any but is preferred to be one related with the clean code architecture.
- **Tests**: Unit Tests are **very important**
- **Documentation**: http://www.tvmaze.com/api
- **API call example**: http://api.tvmaze.com/shows

## Notes
- This assessment must be delivered within **2 days**.
- You can use whatever third party library you want to accomplish these requirements.
- You **must provide** a COMMENTS.txt (plain text) or a COMMENTS.md (Markdown) file at the root of your repository, explaining:
     - Main architecture decisions you've made and a quick explanation of why.
     - List of third party libraries and why you chose each one.
     - What in your code could be improved if you had more time.
     - Mention anything that was asked but not delivered and why, and any additional comments.
- Any questions, please send an email to **recruitment.engineering@avenuecode.com**

## Delivery Instructions

- You must provide your BitBucket username. A free BitBucket account can be created at http://bitbucket.org
- The recruiter will give you read permission to a repository named **ios-challenge**, at https://bitbucket.org/ac-recruitment/ios-challenge
- You must fork this repository into a private repository on your own account and push your code in there.
- Once finished, you must give the user **ac-recruitment** read permission on your repository so that you can be evaluated. Then, please contact back your recruiter and he will get an engineer to evaluate your test.
- After you are evaluated, the recruiter will remove your read permission from the original repository.

Thank you,  
The Avenue Code Recruiting Team