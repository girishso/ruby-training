!SLIDE bullets incremental
# rake command #
* named after _make_
* ![Alt text](../images/jim.jpeg)
* Jim Weirich

!SLIDE commandline incremental
# rake command #
    $ rake -T
      rake about                              # List versions of all Rails frameworks and the environment
      rake assets:clean[keep]                 # Remove old compiled assets
      rake assets:clobber                     # Remove compiled assets
      rake assets:environment                 # Load asset compile environment
      rake assets:precompile                  # Compile all the assets named in config.assets.precompile
      rake cache_digests:dependencies         # Lookup first-level dependencies for TEMPLATE (like messages/show or comments/_comment.html)
      rake cache_digests:nested_dependencies  # Lookup nested dependencies for TEMPLATE (like messages/show or comments/_comment.html)
      rake db:create                          # Create the database from DATABASE_URL or config/database.yml for the current Rails.env (use db:create:all to create all dbs in the c...
      rake db:drop                            # Drops the database using DATABASE_URL or the current Rails.env (use db:drop:all to drop all databases)
      rake db:fixtures:load                   # Load fixtures into the current environment's database
      rake db:migrate                         # Migrate the database (options: VERSION=x, VERBOSE=false, SCOPE=blog)
      rake db:migrate:status                  # Display status of migrations
      rake db:rollback                        # Rolls the schema back to the previous version (specify steps w/ STEP=n)
      rake db:schema:cache:clear              # Clear a db/schema_cache.dump file
      rake db:schema:cache:dump               # Create a db/schema_cache.dump file
      rake db:schema:dump                     # Create a db/schema.rb file that can be portably used against any DB supported by AR
      rake db:schema:load                     # Load a schema.rb file into the database
      rake db:seed                            # Load the seed data from db/seeds.rb
      invoke  active_record

!SLIDE commandline incremental
# rake command #
    $ rake db:create
    $ rake db:drop
    $ rake db:migrate
    $ rake db:seed
    $ rake routes
