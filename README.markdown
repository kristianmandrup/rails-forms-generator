# Rails 3 forms generator

This utility has the goal of outputting (generating) Rails 3 compatible forms from YAML files.
The following Forms DSLs will be supported

* Simpleform
* Formtastic
* Standard Rails forms

## YAML format

There should be support for nested forms:

<pre>
form:
  title: Post form
  fields:
    - name
    - age
    - gender
    - birthday
    form:
      title: Preferences
      fields:
        - theme as:select
        - color as:select        
</pre>

Most of the "usual suspects" of field names should have default mappings, as seen in 'simpleform' ;)

<pre>
  * name      - string  (text field)
  * age       - integer (text field)
  * gender    - boolean (radio)
  * birthday  - date    (date select)
</pre>

## RSpec testing

I plan to use my *forms-spec* gem to test that the generated code is as expected.

## Note on Patches/Pull Requests
 
* Fork the project.
* Make your feature addition or bug fix.
* Add tests for it. This is important so I don't break it in a
  future version unintentionally.
* Commit, do not mess with rakefile, version, or history.
  (if you want to have your own version, that is fine but bump version in a commit by itself I can ignore when I pull)
* Send me a pull request. Bonus points for topic branches.

== Copyright

Copyright (c) 2010 Kristian Mandrup. See LICENSE for details.
