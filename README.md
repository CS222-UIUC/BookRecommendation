# Book Recommendation

By Kaijie Cheng (kaijiec3), Weijia Zhang (weijia4), Zhiyin Liao (zhiyinl2), Yanze Lu (yanzelu2)

## Pitch

In today’s information age, readers are flooded with choices. Online bookstores, digital libraries, and book clubs offer vast catalogs, but the sheer number of options can make it hard to find the perfect book. Traditional recommendation methods, such as bestseller lists or genre categories, often fall short, failing to capture what truly resonates with individual readers.

Our Book Recommendation System uses advanced AI algorithms to learn your reading preferences and deliver personalized book suggestions. Powered by machine learning and data-driven analysis, it examines what you’ve read, what you’ve loved, and even what others with similar tastes are enjoying.

## Functionality

Users can log in on the website to save their preferences.

Users can receive recommendations of books based on books they are interested in.

Users can view basic information of recommended books.

## Components

### Backend

We will write the backend using Python with the Flask framework. All of our team members already know Python, and Flask is widely used for backend code in the Python community, so we can implement it easily. Auth0 is integrated in this app as the login system. The backend has the following components:

Authentication: Login of users according to their linked Google or Microsoft account.

User data manipulation: Send ad hoc user and item features based on frontend data prepared for storing into the database.

Machine learning: Pre-trained, information retrieval-based recommendation engine for user recommendation and user feedback.

Batch processing systems: Hadoop for periodic ingestion of large datasets.

API endpoints: Flask will serve as the interface through which the front-end (or other services) can interact with the recommendation system.

For the Python part, we will use Pytest as our unit test framework. We will manually test the API with Postman.

We will utilize SQLite as the primary database for storing and managing book information in our system. SQLite is a lightweight, serverless SQL database engine that is fully supported by Python, making it a convenient and powerful choice for this project. Its embedded nature allows for seamless integration without the need for a separate database server, simplifying setup and maintenance.

### Frontend

We will write the frontend using JavaScript and Vue.js with Bootstrap. We chose Vue.js because it’s a popular frontend framework with detailed documentation. Also, it’s a lightweight framework compared to React and suitable for small team cooperation. Bootstrap provides us with well-designed CSS styles to make our interface more user-friendly.

Interactive UI: The frontend provides interactive buttons that allow users to perform complex SQL operations/book recommendations with a simple click. Users don’t need to have any programming background and can easily get book recommendations based on individual preference.

Book Display: The frontend also functions as a display window for showcasing relevant book information, allowing users to quickly view and access key details such as the book’s title, author, genre, and more. This streamlined presentation enhances the user experience by making it easy to explore and discover books.

We use Mocha as the test library for the JavaScript part. Mocha doesn't come with an assertion library or mocking framework by default, so we can pair it with any assertion library (like Chai, Should.js, or Assert). This makes Mocha flexible and customizable depending on the testing needs of the project.

We chose to separate our application into a frontend and backend instead of relying on one monolithic application because React makes interactivity easier than writing JavaScript on an HTML page rendered by Django. Essentially, we are using each of our tools for what they’re best at—Django is a great backend, and React a great frontend. This division also makes it easier to develop our user interface in parallel with our backend: we can develop the interface without needing data provided by the backend first, like we would if we only used Django for the whole project.

The frontend sends demands from the user to the backend and shows information from the backend to the user. The data processing part in the backend accepts the demands, decides the data input to the recommendation model, and sends the information needed to be shown to the frontend. It also saves the user’s information and output of the recommendation model to the database. The recommendation model is trained to give recommendations based on the user’s favorite books.

## Weekly Planning

Week # (Date)

Tasks

Week 1 (9/20-9/26)

1. Polish rough proposal

Get familiar with backend and frontend language, especially exploring realistic examples applying those frameworks on database systems |
| Week 2 (9/27-10/3) | 1. Learn similar example’s program architecture, including how they integrate their frontend, backend, database, etc.

Make a UML graph to display class structure and lifecycle of software using draw.io or relevant tools |
| Week 3 (10/4-10/10) | 1. Design a user-friendly UI/UX layout for frontend, integrating how UI elements are arranged and what interaction feature it should have

Explore relevant books training set for database usage |
| Week 4 (10/11-10/17) | 1. Explore training method for book recommendation or relevant examples

Create basic UI layout including homepage |
| Week 5 (10/18-10/24) | 1. Train recommendation model based on existing training set

Create the book database with SQLite |
| Week 6 (10/25-10/31) | 1. Test model’s performance using the created database, evaluate it and retrain the model if needed until achieving certain quality based on our human feedback

Implement relevant interface for backend to perform relevant SQL queries or inference using trained model |
| Week 7 (11/1-11/7) | 1. Create URL request for communication between frontend and backend

Create buttons on frontend to run the recommendation process via clicking |
| Week 8 (11/8-11/14) | 1. Integrate more features, for example, recommend based on user’s preference between frontend and backend to interact with the trained model

Create login page and implement search books feature in frontend |
| Week 9 (11/15-11/21) | 1. Test the whole process and ensure the smooth user experience for finding the book they like using our recommendation system

Fix potential bugs |
| Week 10 (11/22-11/28) | 1. Fix potential bugs

Prepare presentation materials

Leave buffer time for any risk |

Potential Risks

We might face challenges when trying to call backend methods from the frontend, as this is new territory for us. If we run into problems, we intend to consult our mentor, who has experience in this area. We estimate that the time impact of this is 1-2 days, but it should not affect our overall progress.

The recommendation model may be inaccurate or even fail. If we encounter this, we will try our best to train and fix it. The time impact of this would be 1-2 weeks. If we cannot fix it, we will probably drop some of the recommendation functions.

The development language is new for us, so we may have some issues in writing the code or face program crashes. If we encounter this, we will contact our mentor for help since he has experience with this. The time impact of this may be 1-2 days and would not affect our overall progress.

## Teamwork

To better train our software development skills, everyone in the team will be responsible for every component of the website. Each functionality will be divided into levels of main functions and sections to be distributed to each member. We will create a GitHub repository to manage the progress of every member. This allows us to collaborate efficiently in writing code.

We will hold a weekly meeting with our mentor to make sure everything is on track. We will schedule a time to work together in person on Thursday afternoon in the library. We review what we have done this week and distribute next week's work to every teammate. In the rest of the week, we work individually on our tasks. Additionally, we have a Slack workspace to communicate if we encounter any problems. When we face any problem, we encourage our teammates to immediately communicate with other teammates and the mentor to solve it. If we face a big issue in developing the program, we will consider increasing working time and reassigning tasks in order to keep everything on track.

Continuous Integration

Use PyTest for unit, integration, and functional testing.

Use Flake8 to check adherence to PEP 8 standards.

Use Coverage.py to measure code coverage.

Pull Request Workflow:

Branch from main following a clear naming convention.

Create PRs with sufficient testing, request review from peers, and ensure coverage and style checks pass before merging.

Use "Squash and Merge" to keep the main branch clean.
