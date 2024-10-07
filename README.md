# BookRecommendation
 By Kaijie Cheng (kaijiec3), Weijia Zhang(weijia4), Zhiyin Liao (zhiyinl2), Yanze Lu (yanzelu2)
 Pitch
 In today’s information age, readers are flooded with choices. Online bookstores, digital libraries, and
 book clubs offer vast catalogs, but the sheer number of options can make it hard to find the perfect book.
 Traditional recommendation methods, such as bestseller lists or genre categories, often fall short, failing
 to capture what truly resonates with individual readers.
 Our Book Recommendation System uses advanced AI algorithms to learn your reading preferences and
 deliver personalized book suggestions. Powered by machine learning and data-driven analysis, it
 examines what you’ve read, what you’ve loved, and even what others with similar tastes are enjoying.
 Functionality
 1. Users can login on the website to save their preferences
 2. Users can receive recommendations of books based on books they are interested in
 3. Users can view basic information of recommended books
 Components
 ● Backend: Wewill write the backend using Python with the Flask framework. All of our team
 members already know Python, and Flask is widely used for backend code in the Python
 community, so we can implement it easily with this code. Auth0 is integrated in this app as the
 login system. The backend has following components:
 ○ Authentication
 ■ Loginofusers according to their linked Google or Microsoft account.
 ○ Userdata manipulation
 ■ Sendadhocuser and item features based on frontend data prepared for storing
 into database
 ○ Machinelearning
 ■ Pre-trained, Information Retrieval based recommendation engine for user
 recommendation and user feedback
 ○ Batchprocessing systems
 ■ Hadoopfor periodic ingestion of large datasets.
 ○ APIendpoints
 ■ Flaskwill serve as the interface through which the front-end (or other services)
 can interact with the recommendation system.
 For the Python part, we will use Pytest as our unit test framework. We will manually test the API
 with Postman.
 ● Wewillutilize SQLite as the primary database for storing and managing book information in our
 system. SQLite is a lightweight, serverless SQL database engine that is fully supported by
 Python, making it a convenient and powerful choice for this project. Its embedded nature allows
for seamless integration without the need for a separate database server, simplifying setup and
 maintenance.
 ● Frontend: We will write the frontend using Javascript and Vue.js+bootstrap. We chose Vue.js
 because it’s a popular frontend with detailed documentation. Also, it’s a lite framework compared
 to React and suitable for small team cooperation. Bootstrap provides us with well-designed css
 style to make our interface more well-designed and user-friendly
 ○ Interactive UI: frontend provides interactive buttons that allow users to do complex SQL
 operation/book recommendation with a simple click. Users don’t need to have any
 programming background and can easily get the book recommended based on individual
 preference.
 ○ BookDisplay: The frontend also functions as a display window for showcasing relevant
 book information, allowing users to quickly view and access key details such as the
 book’s title, author, genre, and more. This streamlined presentation enhances the user
 experience by making it easy to explore and discover books.
 Weuse Mocha as the test library on the Javascript part. Mocha doesn't come with an assertion
 library or mocking framework by default, so we can pair it with any assertion library (like Chai,
 Should.js, or Assert). This makes Mocha flexible and customizable depending on the testing needs of the
 project.
 Wechose to separate our application into a frontend and backend instead of relying on one monolithic
 application because React makes interactivity easier than writing JavaScript on an HTML page rendered
 by Django; essentially, we are using each of our tools for only what they’re best at– Django is a great
 backend, and React a great frontend. This division also makes it easier to develop our user interface in
 parallel with our backend: we can develop the interface without needing data provided by the backend
 first, like we would if we only used Django for the whole project.
Thefrontendsendsdemandsfromtheusertothebackendandshowsinformationfromthebackendtothe
 user.Thedataprocessingpartinthebackendacceptsthedemands,decidesthedatainputtothe
 recommendationmodel,andsendstheinformationneededtobeshowntothefrontend.Italsosavesthe
 user’sinformationandoutputoftherecommendationmodeltothedatabase.Therecommendationmodel
 istrainedtogiverecommendationsbasedontheuser’sfavoritebooks.
 WeeklyPlanning
 Week#(Date) Tasks
 Week1(9/20-9/26) 1.Polishroughproposal
 2.Getfamiliarwithcorrespondingbackendandfrontendlanguage,especiallyexploringthe
 realisticexamplesapplyingthoseframeworkondatabasesystem
 Week2(9/27-10/3)
 1.Learnsimilarexample’sprogramarchitecture,includinghowtheyintegratetheirfrontend,
 backend,database,etc
 2.MakeanUMLgraphtodisplayclassstructureandlifecycleofsoftwareusingdraw.ioor
 relevanttools
 Week3(10/4-10/10) 1.Designauser-friendlyUI/UXlayoutforfrontend,invergatinghowUIelementsare
 arrangedandwhatinteractionfeatureitshouldhave
 2.Explorerelevantbookstrainingsetfordatabaseusage
 Week4(10/11-10/17) 1.Exploretrainingmethodforbookrecommendationorrelevantexamples
 2.Createbasicuilayoutincludinghomepage
 Week5(10/18-10/24) 1.Trainrecommendationmodelbasedonexistingtrainset
 2.CreatethebookdatabasewithSqlite.
 Week6(10/25-10/31) 1. Testmodel’susingthecreateddatabase,evaluateitandretrainthemodelifneeded
 untilachievecertainqualitybasedonourhumanfeedback
 2. ImplementrelevantinterfaceforbackendtodorelevantSQLqueryorinferenceusing
 trainedmodel
 Week7(11/1-11/7) 1.Createurlrequestforcommunicationbetweenfrontendandbackend
 2.Createbuttonsonfrontendtoruntherecommendationprocessviaclicking
 Week8(11/8-11/14) 1.Integratemorefeature,forexample,recommendbasedonuser’spreferencebetween
 frontendandbackendtointeractwiththetrainedmodel
 2. Createloginpageandimplementsearchbooksfeatureinfrontend
 Week9(11/15-11/21) 1. Testthewholeprocessandensurethesmoothuserexperienceforfindingthebook
 theirlikeusingourrecommendationsystem
 2. Fixpotentialbugs
 Week10
 (11/22-11/28) 1.Fixpotentialbugs
 2.Preparepresentationmaterials
3. Leave buffer time for any risk
 Potential Risks
 1. Wemight face challenges when trying to call backend methods from the frontend, as this is new
 territory for us. If we run into problems, we intend to consult our mentor, who has experience in
 this area. We estimate that the time impact of this is 1-2 days, but it should not affect our overall
 progress.
 2. Therecommendation model may be inaccurate or even crushed. If we encounter this, we will try
 our best to train and fix it. The time impact of this would be 1-2 weeks. If we cannot fix it, we
 will probably drop some of the recommendation functions.
 3. Thedeveloping language is new for us so we may have some issues in writing the code or the
 program crash. If we encounter this, we will contact our mentor for help since he has experience
 with this. The time impact of this may be 1-2 days and would not affect our overall progress.
 Teamwork
 To better train our software development skills, everyone in the team will be responsible for every
 component of the website. Each functionality will be divided into levels of main functions and sections to
 be distributed to each member. We will create a github repository to manage the progress of every
 member. This allows us to collaborate efficiently in writing code.
 Wewill hold a weekly meeting with our mentor to make sure everything is on track. We will schedule a
 time to work together in person on Thursday afternoon in the library. We review what we have done this
 week and distribute next week's work to every teammate. In the rest of the week, we work individually on
 our tasks. Additionally, we have a Slack workspace to communicate if we encounter any problems. When
 we face any problem, we encourage our teammates to immediately communicate with other teammates
 and the mentor to solve it. If we face a big issue in developing the program, we will consider increasing
 working time and reassigning tasks in order to keep everything on track .
 Continuous Integration
 Use PyTest for unit, integration, and functional testing.Use Flake8 to check adherence to PEP 8
 standards.Use Coverage.py to measure code coverage.
 Pull Request Workflow:
 ● Branchfrom main following a clear naming convention.
 ● Create PRs with sufficient testing, request review from peers, and ensure coverage and style
 checks pass before merging.
 ● UseSquashand Merge to keep the main branch clean.
