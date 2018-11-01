### active_attr
---
https://github.com/cgriego/active_attr


```ruby
class Person
  include ActiveAttr::Attributes
  attribute :first_name
  attribute :last_name
end
person = Person.new
person.first_name = "tky"
person.last_name = "tky"
person.attributes 

class Person
  include ActiveAttr::AttributeDefaults
  attribute :first_name, :default => "tky"
  attribute :last_name, :default => "Doe"
end
person = Person.new
person.first_name
person.last_name

class Person
end
person = Person.new
person.first_nmae = "tky"
person.first_name?
person.last_name?

class Person
end
person = Person.new
person.age = "29"
person.age

class Person
end
Person.model_name.plural
person = Person.new
person.valid?
person.errors.full_messages

class Person
end
person = Person.new do |p|
end
person.first_name
person.last_name

class Person
end
Person.logger = Logger.new(STDOUT)
Person.logger?
Person.logger.info ""
person = Person.new
person.logger?
person.logger = Logger.new(STDOERR)
person.logger.warn ""

class Person
end
person = Person.new()
persson.attributes = {}
person.first_name
person.last_name

class Person
end
person = Person.new().permit()
person.first_name
person.last_name

class Person
end
person = Person.new()
person.first_name
person.last_name

class Person
end

class Person
end

gem "active_attr"

require "active_attr/rspec"
describe Person do
  it do
    should have_attribute(:first_name).
      of_type(String).
      with_default_value_of("tky")
  end
end

```

```
```

```
```

