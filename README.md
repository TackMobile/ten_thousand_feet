# TenThousandFeet

Ruby wrapper for the [10,000ft API (BETA)](http://10kft.github.io/api-documentation).

## Installation

    gem 'ten_thousand_feet'

Or

    gem install ten_thousand_feet

## Setup

    require 'ten_thousand_feet'

    # Initialize a new 10,000ft client
    client = TenThousandFeet.new(auth: YOUR_AUTH_TOKEN)

# API Methods
    # Note: 'options' will be different for each method. Check the official API documentation for details on the available options for each call.

    # 'options' should be passed in as a hash:
    # { name: 'Austin Powers', client: 'Dr. Evil' }

## Users

    client.get_users(options)
    client.show_user(user_id, options)
    client.update_user(user_id, options)
    client.create_user(options)

## User Status

    client.get_user_statuses(user_id, options)
    client.create_user_status(user_id, options)

## Assignments
    
    client.get_assignments(user_id, options)
    client.show_assignment(assignment_id, user_id, options)
    client.create_assignment(project_id, user_id, options)
    client.delete_assignment(assignment_id, user_id, options)

## Projects

    client.get_projects(options)
    client.show_project(project_id, options)
    client.update_project(project_id, options)
    client.create_project(options)
    client.delete_project(project_id, options)
    client.get_project_time_entries(project_id, options)
    client.get_project_users(project_id, options)

## Phases
    
    client.get_phases(project_id, options)
    client.create_phases(project_id, options)
    client.update_phases(project_id, phase_id, options)

## Time Entries

    client.get_time_entries(user_id, options)
    client.show_time_entry(time_entry_id, user_id, options)
    client.update_time_entry(time_entry_id, user_id, options)
    client.create_time_entry(user_id, options)
    client.delete_time_entry(time_entry_id, user_id, project_id, options)

## To-Do

* Budget Items
* Budget Item Categories
* Tags Per Project
* Tags Per User

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
