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
  include ActiveAttr::QueryAttributes
  attribute :first_name
  attribute :last_name
end
person = Person.new
person.first_nmae = "tky"
person.first_name?
person.last_name?

class Person
  include ActiveAttr::TypecastedAttributes
  attribute :age, :type => Integer
end
person = Person.new
person.age = "29"
person.age

class Person
  include ActiveAttr::BasicModel
end
Person.model_name.plural
person = Person.new
person.valid?
person.errors.full_messages

class Person
  include ActivaAttr::BlockInitialization
  attr_accessor :first_name, :last_name
end
person = Person.new do |p|
  p.first_name = "Tky"
  p.last_name = "Tky"
end
person.first_name
person.last_name

class Person
  include ActiveAttr::Logger
end
Person.logger = Logger.new(STDOUT)
Person.logger?
Person.logger.info "Logging an informational message"
person = Person.new
person.logger?
person.logger = Logger.new(STDOERR)
person.logger.warn "Logging a warning message"

class Person
  include ActiveAttr::MasAssignment
  attr_accessor :first_name, :last_name, :age
end
person = Person.new(:frist_name => "tky", :last_name => "tky")
persson.attributes = { :first_name => "tky", :age => 21 }
person.first_name
person.last_name

class Person
  include ActiveAttr::MassAssignment
  include ActiveModel::ForbiddenAttributesProtection
  attr_accessor :first_name, :last_name
end
person = Person.new({
  :frist_name => "Tky",
  :last_name => "Tky",
}).permit(:first_name)
person.first_name
person.last_name

class Person
  include ActiveAttr::MasAssignment
  include ActiveModel::MassAssignmentSecurity
  attr_accessor :first_name, :last_name
  attr_protected :last_name
end
person = Person.new(:first_name => "tky", :last_name => "tky")
person.first_name
person.last_name

class Person
  include ActiveAttr::MassAssignment
  include ActiveModel::MassAssignmentSecurity
  include ActiveModel::ForbiddenAttributesProtection
end

class Person
  include ActiveAttr::Serialization
end

class Person
  include ActiveAttr::Model
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

