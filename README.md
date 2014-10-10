How We Work
===========


## Formatting

As usual we use [bbatsov/ruby-style-guide](https://github.com/bbatsov/ruby-style-guide), 
but have some specific usage:

* Limit lines to 104 characters, in order to remove horizontal scrolling on GitHub when we are doing code review
* Align parameters like:

```ruby
# not so bad
def send_mail(source)
  Mailer.deliver(
    to: 'bob@example.com', from: 'us@example.com'
  )
end

# good
def send_mail(source)
  Mailer.deliver(to: 'bob@example.com',
                 from: 'us@example.com',
                 subject: 'Important message',
                 body: source.text)
end

# good (normal indent)
def send_mail(source)
  Mailer.deliver(
    to: 'bob@example.com',
    from: 'us@example.com',
    subject: 'Important message',
    body: source.text
  )
end
```

