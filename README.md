### forkoff 
---
https://github.com/ahoward/forkoff

```
gem install forkoff

```


```ruby
require 'forkoff'
%w( hey you ).forkoff!(|word| puts "#{ word } form #{ Process.pid }")

require 'forkoff'
a = Time.now_to_f
results =
  (0..7).forkoff do |i|
    sleep 1
    i ** 2
  end
b = Time.now.to_f
elapsed = b - a
puts "elapsed: #{ elapsed }"
puts "results: #{ results.inspect }"

```

```
```
