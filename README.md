# CourseCompass

Course registration, the beginning of many hours of research in search for the perfect course, can be a source of frustration for many students. Oftentimes, students are unsure of what courses they'll perform best in and lack the definitive tools to make less educated guesses and to start making data-backed decisions on the courses that align best with their experience and interests.

If you are one of these folks, we have the solution for you! 

**CourseCompass** provides Columbia University students with a personalized course recommendation and career planning tool. Using Collaborative Filtering, our algorithms are able to intake your existing grades and recommend new courses to take based on the topics and grades you've received thus far. Search through a catalog of existing courses and read professor reviews to get a better grasp of the academic experience they hope to offer, but if you find yourself lost, you can always have CourseCompass recommend suggestions instead!

Built from the ground-up in Ruby on Rails, CourseCompass is fast and extensive in its features, empowering students to make informed decisions regarding their next courseload.

## Demo Deployments

### Iteration 1
Basic page view for courses, seeds, and recommendation methods.
- [Heroku Demo - Iteration 1](https://course-compass-iter1-cc03da1256a5.herokuapp.com)

### Iteration 2
Added login functionality, user info page, and course enrollments.
- [Heroku Demo - Iteration 2](https://course-compass-iter2-ea6d54216710.herokuapp.com)

### Demo Day
Final iteration with all features included.
- [Heroku Demo - Demo Day](https://course-compass-demo-fbf53d190587.herokuapp.com)

### Final 
Final iteration with all tests included, bug fixed.
- [Heroku Demo - Final](https://course-compass-final-0cfa67aed3b0.herokuapp.com/)

## Features

- **Course Browsing:** Browse available courses and their details.
- **Login and User Profiles:** Manage user information and course history.
- **Course Enrollment and History:** Add and edit past course enrollments.
- **Personalized Recommendations:** Receive course recommendations based on history.

## Coverage Report

The current test coverage is at **90.34%**. Detailed reports are available in `coverage/index.html`.

## Team Members

| Name           | UNI    |
|----------------|--------|
| Esteeven Cepeda | enc2129|
| Orr Avrech     | oa2429 |
| Kaiyuan Hou    | kh3119 |
| Kevin Medina   | km3628 |

## Installation

### Cloning the Repository
```bash
git clone https://github.com/Hou-Kaiyuan/CourseCompass
cd CourseCompass
```

### Installing Ruby on Linux
For Linux environments (tested on Codio Empty Stack), run the following script:
```bash
bash setup_ruby.sh

export PATH="$HOME/.rbenv/bin:$PATH"
eval "$(rbenv init -)"
rbenv global 2.6.6

# Check that ruby version is 2.6.6
ruby -v
```
Alternatively, follow the manual installation steps in the script.

## Setup and Local Testing

### 1. Installing Gems and Dependencies
Execute:
```bash
bash coursecompass.sh
```
Or follow the manual installation steps in the script.

### 2. Database Setup and Running Tests
```bash
bundle exec rake db:migrate db:test:prepare db:seed
bundle exec rspec
bundle exec cucumber
```

### 3. Running Locally or on a Public Server
```bash
rails s -b 0.0.0.0 -p 3000
# or
bundle exec rackup --host 0.0.0.0 --port 3000
```

## Heroku Deployment

Ensure [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli) is installed. Follow these steps for deployment:
```bash
git clone https://github.com/Hou-Kaiyuan/CourseCompass
cd CourseCompass
heroku create
heroku git:remote -a <app_name>
heroku stack:set heroku-20
heroku addons:create heroku-postgresql
git push heroku master
heroku run rake db:migrate db:seed
heroku logs
heroku run bash
```

## GitHub Repository
[CourseCompass on GitHub](https://github.com/Hou-Kaiyuan/CourseCompass)


## Demo
![ezgif-1-27f3632437](https://github.com/user-attachments/assets/fdb66461-ec12-462e-ac89-4fba525e1e9a)


