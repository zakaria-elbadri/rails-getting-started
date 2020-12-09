# Welcome to Rails

Rails is a web-application framework that includes everything needed to create
database-backed web applications according to the Model-View-Control pattern.

This pattern splits the view (also called the presentation) into "dumb" templates
that are primarily responsible for inserting pre-built data in between HTML tags.
The model contains the "smart" domain objects (such as Account, Product, Person,
Post) that holds all the business logic and knows how to persist themselves to
a database. The controller handles the incoming requests (such as Save New Account,
Update Product, Show Post) by manipulating the model and directing data to the view.

In Rails, the model is handled by what's called an object-relational mapping
layer entitled Active Record. This layer allows you to present the data from
database rows as objects and embellish these data objects with business logic
methods.

The controller and view are handled by the Action Pack, which handles both
layers by its two parts: Action View and Action Controller. These two layers
are bundled in a single package due to their heavy interdependence. This is
unlike the relationship between the Active Record and Action Pack that is much
more separate. Each of these packages can be used independently outside of
Rails.

# Getting Started

1. At the command prompt, start the Rails application using the <tt>rails</tt> command: rails start
2. Go to http://localhost:3000/ and get "Welcome aboard: You're riding the Rails!"

# Description of Contents

* **app**
Holds all the code that's specific to this particular application.

* **app/controllers**
Holds controllers that should be named like weblogs_controller.rb for automated URL mapping.
All controllers should descend from ApplicationController which itself descends from ActionController::Base.

* **app/models**
Holds models that should be named like post.rb.
Most models will descend from ActiveRecord::Base.

* app/views
  Holds the template files for the view that should be named like
  weblogs/index.html.erb for the WeblogsController#index action. All views use eRuby
  syntax.

* app/views/layouts
  Holds the template files for layouts to be used with views. This models the common
  header/footer method of wrapping views. In your views, define a layout using the
  <tt>layout :default</tt> and create a file named default.html.erb. Inside default.html.erb,
  call <% yield %> to render the view using this layout.

* app/helpers
  Holds view helpers that should be named like weblogs_helper.rb. These are generated
  for you automatically when using script/generate for controllers. Helpers can be used to
  wrap functionality for your views into methods.

* config
  Configuration files for the Rails environment, the routing map, the database, and other dependencies.

* db
  Contains the database schema in schema.rb.  db/migrate contains all
  the sequence of Migrations for your schema.

* doc
  This directory is where your application documentation will be stored when generated
  using <tt>rake doc:app</tt>

* lib
  Application specific libraries. Basically, any kind of custom code that doesn't
  belong under controllers, models, or helpers. This directory is in the load path.

* public
  The directory available for the web server. Contains subdirectories for images, stylesheets,
  and javascripts. Also contains the dispatchers and the default HTML files. This should be
  set as the DOCUMENT_ROOT of your web server.

* script
  Helper scripts for automation and generation.

* test
  Unit and functional tests along with fixtures. When using the script/generate scripts, template
  test files will be generated for you and placed in this directory.

* vendor
  External libraries that the application depends on. Also includes the plugins subdirectory.
  If the app has frozen rails, those gems also go here, under vendor/rails/.
  This directory is in the load path.
