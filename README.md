# CS-360


    Briefly summarize the requirements and goals of the app you developed. What user needs was this app designed to address?

  The intent was to build a very simple inventory management application that supports user registration and login, CRUD operations on an inventory item database, an intuitive inventory display, and a notification feature that indicates when stocks fall to zero. The app was designed with small retail operations in mind. Anything from a boutique to a restaurant to an independent Shopify operator is considered. 
    
    What screens and features were necessary to support user needs and produce a user-centered UI for the app? How did your UI designs keep users in mind? Why were your designs successful?

  The app opens on a login activity wherein users are prompted for their credentials via EditText widgets.
  
  A button on the login activity redirects to the user registration activity. This screen accepts new credentials via EditTexts and saves users to the user database. Users can then navigate back to the login screen by a convenient button.
  
  Upon login, the inventory screen is displayed. Coded in the application is a grid view widget as well as a grid_cell.xml file intended to populate the grid view (with each grid_cell itself populated by item details).
  
  Also on the inventory activity are floating buttons.
  
  The first floating button navigates the user to the screen where they are prompted to decide whether to turn on SMS notifications for out-of-stock items (yet unimplemented). The user may select "Yes" (unhandled) or "No" to navigate back to the inventory screen.
  
  The second floating button button navigates the user to an activity for adding items: again, EditText widgets accept input and there is a button for each of adding the items and navigating back to the inventory view.

  I intended for this application to be intuitive to navigate and unintimidating to users who may not be tech savvy. I believe clearly-labeled buttons, minimal navigation requirements, and unambiguous toast messages help this app accomplish these goals.
    
    How did you approach the process of coding your app? What techniques or strategies did you use? How could those techniques or strategies be applied in the future?

  Commented code block headers helped me keep track of app functionality and FIXME statements helped me work towards discrete, manageable goals.
  
  The coding practices I used were straightforward, almost all coming from the Android Studio official documentation and textbook examples. I intend to use these skills and even the templates I created to perfect this app as well as to build more in the future.
    
    How did you test to ensure your code was functional? Why is this process important, and what did it reveal?

  The Android Studio inbuilt emulator was my primary modus of testing the app. Most changes to the code are followed by an emulation and comprehensive run-through of all the features (luckily very simple to do due to the app's minimalist design, as intended). It was surprising how some seemingly innocuous code changes could break button callbacks or activities that seemed utterly unrelated to the code that was changed.
    
    Consider the full app design and development process from initial planning to finalization. Where did you have to innovate to overcome a challenge?

  Looking back at my early projects in this course, I can see that I had trouble with everything from getting layouts to constrain properly to implementing onClickListeners. Learning to create with Android Studio was its own challenge, albeit an incredibly fun one.
  
  When it came to the app design and development, I was challenged by the inventory view widget. I found myself getting familiar with many methods to populate data into a view, especially ArrayLists and inbuilt lists. I attempted to iteratively query the SQLite database to populate both types of list to provide data to the view cells. Unfortunately, something is keeping these methods from succeeding for me (it could even be a failure to nest the grid_cell.xml into activity_inventory.xml's GridView). I hit a wall with this process and failed to implement the feature in time for submission. Next, I am going to attempt loading data directly from iterative queries, but I am unsure how this should be coded and will need to keep innovating, trying, and failing to get it right.
  
    In what specific component of your mobile app were you particularly successful in demonstrating your knowledge, skills, and experience?

  I am proud of my user and item database functionalities. Usernames function as primary keys and thus the app can return a "username is already taken" error at user registration.
  
  I originally had to include a debug feature to jump from the login screen directly to the inventory view without login credentials because the database was not implemented correctly right off the bat. When I finally got verification and exception handling working (and it was very exciting to see a successful registration and login for the first time) it was a breeze to implement the inventory database, and I now feel very confident in these skills. (It does help that my other course this semester focused on database querying and CRUD operations, as well; if anything, I should have implemented more CRUD operation handling before upload, although it would have been invisible as the interactive view widget and its add/delete/update buttons do not exist yet.)
