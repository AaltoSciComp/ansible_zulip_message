ansible_zulip_message
=====================

This helper role will send Zulip messages via Zulip REST API.

Requirements
------------

None.

Role Variables
--------------

The following variables need to be set when calling the role:


| Parameter         | Example                                      | Explanation               |
|-------------------|----------------------------------------------|---------------------------|
| zulip_server_url  | "https://test.zulipchat.com/api/v1/messages" | Zulip API endpoint        |
| zulip_user        | "my-bot@test.zulipchat.com"                  | Zulip Bot user            |
| zulip_api_key     | "my-api-key"                                 | Zulip Bot API key         |
| zulip_stream      | "my stream"                                  | Stream to post into       |
| zulip_topic       | "my topic"                                   | Topic to post into        |
| message           | "my message"                                 | Message that will be sent |


Dependencies
------------

None

Example Playbook
----------------

```yml
---

- name: Send a test zulip message
  hosts: localhost

  roles:
    - role: ansible_zulip_message
      vars:
        zulip_server_url: https://test.zulipchat.com/api/v1/messages
        zulip_user: my-bot@test.zulipchat.com
        zulip_api_key: my-api-key
        zulip_stream: my stream
        zulip_topic: my topic
        message: This is a test message from ansible
```

License
-------

MIT

Author Information
------------------

Simo Tuomisto, Aalto University 2024
