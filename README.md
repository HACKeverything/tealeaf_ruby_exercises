# tealeaf_ruby_exercises

2.1.2 :002 > arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
 => [1, 2, 3, 4, 5, 6, 7, 8, 9, 10] 
2.1.2 :003 > arr.each { |e| puts e }
1
2
3
4
5
6
7
8
9
10
 => [1, 2, 3, 4, 5, 6, 7, 8, 9, 10] 
2.1.2 :004 > arr.each { |e| puts e if e > 5 }
6
7
8
9
10
 => [1, 2, 3, 4, 5, 6, 7, 8, 9, 10] 
2.1.2 :005 > arr.select { |num| num % 2 != 0 }
 => [1, 3, 5, 7, 9] 
2.1.2 :006 > arr.push(11)
 => [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11] 
2.1.2 :007 > arr.unshift(0)
 => [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11] 
2.1.2 :008 > arr.pop
 => 11 
2.1.2 :009 > arr
 => [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10] 
2.1.2 :010 > arr.push(3)
 => [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 3] 
2.1.2 :011 > arr
 => [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 3] 
2.1.2 :012 > arr.uniq
 => [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10] 
2.1.2 :013 > arr
 => [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 3] 
2.1.2 :014 > arr.uniq!
 => [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10] 
2.1.2 :015 > arr
 => [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10] 
 
Array has "index" start from 0, and every index associate with a element
Hash is composed of key value pairs, and the order don't matter

hash = { :name => 'bob' }     # old version
hash = { name: 'bob' }        # new version

h[:b]

h[:e] = 5

h.delete_if { |k, v| v < 3.5 }

hash = { names: ['bob', 'joe', 'susan'] }
arr = [ {name: 'bob'}, {name: 'joe'}, {name: 'susan'} ]

http://ruby-doc.org/ is great.
I can search any method or class by filter


2.1.2 :005 > contact_data.flatten!
 => ["joe@email.com", "123 Main st.", "555-123-4567", "sally@email.com", "404 Not Found Dr.", "123-234-3454"] 
2.1.2 :006 > contacts.each do |name, hash|
2.1.2 :007 >       fields.each do |field|
2.1.2 :008 >           hash[field] = contact_data.shift
2.1.2 :009?>       end
2.1.2 :010?>   end
 => {"Joe Smith"=>{:email=>"joe@email.com", :address=>"123 Main st.", :phone=>"555-123-4567"}, "Sally Johnson"=>{:email=>"sally@email.com", :address=>"404 Not Found Dr.", :phone=>"123-234-3454"}} 
 
 2.1.2 :011 > puts "Joe's email is: #{contacts["Joe Smith"][:email]}"
Joe's email is: joe@email.com
 => nil 
2.1.2 :013 > puts "Sally's phone is: #{contacts["Sally Johnson"][:phone]}"
Sally's phone is: 123-234-3454
 => nil 

14. 

contacts.each_with_index do |(name, hash), idx|
  fields.each do |field|
    hash[field] = contact_data[idx].shift
  end
end

arr.delete_if { |word| word.start_with?("s", "w") }

2.1.2 :001 > a = ['white snow', 'winter wonderland', 'melting ice',
2.1.2 :002 >          'slippery sidewalk', 'salted roads', 'white trees']
 => ["white snow", "winter wonderland", "melting ice", "slippery sidewalk", "salted roads", "white trees"] 
2.1.2 :003 > a = a.map { |pairs| pairs.split }
 => [["white", "snow"], ["winter", "wonderland"], ["melting", "ice"], ["slippery", "sidewalk"], ["salted", "roads"], ["white", "trees"]] 
2.1.2 :004 > a = a.flatten
 => ["white", "snow", "winter", "wonderland", "melting", "ice", "slippery", "sidewalk", "salted", "roads", "white", "trees"] 

These hashes are the same!  # Hashes are not meant to be in a certain order 
