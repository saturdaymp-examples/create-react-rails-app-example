# Create a React-Rails App Example
This is working example for the [Today I Learned How to Create a React-Rails App](https://nftb.saturdaymp.com/today-i-learned-how-to-create-a-react-rails-app/) blog post.

# Quickstart
Install [Docker](https://docs.docker.com/install/) and then build the containers by running the following command:

````
docker-compose build web
````

After the containers are built you need to update the yarn dependencies and create the databases:

````
docker-compose run web bash

yarn install
rake db:create
exit
````

You can test if everything is working correctly by running the container and navigating to localhost:3000.  You should see the "Welcome to Rails" page if everything is working correctly.

````
docker-compose up web
````

# Contributing 
If you have any questions, notice a bug, or have a suggestion/enhancment please let me know by opening a [issue](https://github.com/saturdaymp-examples/create-react-rails-app-example/issues) or [pull request](https://github.com/saturdaymp-examples/create-react-rails-app-example/pulls).

# Acknowledgements
Thanks to folks who created [React-Rails](https://github.com/reactjs/react-rails).
