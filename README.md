# Templates and config files storage

Store templates and config files for reuse in future.

## **How to Use**

### **Directory Structure**
```
ruby_and_rails_templates
│
│
└─── docker_set_up
|   |
|   └─── rails_with_mongo
|   |
|   └─── rails_with_postgresql
|   
|   
└─── code_review_set_up
|   │
|   └─── rubocop                       (Ruby static code analyzer and formatter)
|   |   │   
|   │   └─── default
|   |       |
|   │       └─── .rubocop_base.yml
|   │       └─── .rubocop.yml
|   |
|   └─── fasterer                      (Ruby suggest some speed improvements)
|   |    |
|   |    └─── default/.fasterer.yml
|   |
|   └─── reek                          (Code smell detector for Ruby)
|   |    |
|   |    └─── default/.reek.yml
|   |
|   └─── rubycritic                    (Ruby code quality reporter)
|        |
|        └─── default/.rubycritic.yml
|   
└─── readme_templates
    │
    └─── default
        │ README.md
```


https://evilmartians.com/chronicles/anycable-1-0-four-years-of-real-time-web-with-ruby-and-go
