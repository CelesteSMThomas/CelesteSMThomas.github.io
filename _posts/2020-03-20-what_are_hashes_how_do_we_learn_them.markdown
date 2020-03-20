---
layout: post
title:      "What are Hashes? How do we learn them?"
date:       2020-03-20 15:52:53 +0000
permalink:  what_are_hashes_how_do_we_learn_them
---

Hashes

When looking at hashes they can be intimidating. You see a bunch of curly brackets and colons. They look foreign. 

```
hash = {"key" => "value" , "second key" => "second value" }
```

We have the "hash" being the main name of the hash. Then we have our first key & value pair, then our second key value pair. Hashes allow us to store TONS of information. I think for me hashes are pretty straight foward the issue I faced was the syntax. I would suggest spending A LOT of time making them and getting used to making them because once you get hashes down you then learn about Nested Hashes. Which again, I don't neccessarily believe that Nested Hashes are difficult it's just the presentation is intimidating.

For example a Nested Hash looks like such:

```
celestes_favorites = {

  food: ["mac and cheese", "steak", "salmon"], 
	
  activity: ["code", "walk", "play with dog", "sleep", "video games", "read"]
	
	show: ["Grey's Anatomy", "Twenties", "This is Us" ]
	
}
```

For clarity I've separated the syntax one line at a time. Nested Hashes allows us to store more than just the average key pointing to one value pair. In this example we want to list some of the key components of Flatiron School. We have the keys being - ```food:        activity:       show: ``` Let's note that keys in nested hashes end with a colon ( : ). As well as when one particular key pair value is complete it ends as such: ( ], ). With a comma separating the next pair. Be mindful of the little details. These particular keys point to an array. But how do we return just the instructor key you ask?
First, we call the main name of the has ``` celestes_favorite``` then on that we call the key name. See below:

```
celestes_favoritesl[:show]

#=>  ["Grey's Anatomy", "Twenties", "This is Us" ]
```

If you didn't catch it look at where the colon is when calling instructors IN THE FRONT. This is one example on how the syntax can throw you off if you don't learn it.

But how do we call just one specific show? Let's say "Twenties" Because we know the exact location; We know its a part of celestes_favorites we know its a part of show: and we know its the 1st in index location. We can call it like this:

```
celestes_favorites[:show][1]

#=> "Twenties"
```


Iterating over a hash
Below is a simple iteration over a hash using each. Which is just as we would do with an array.

```
celestes_favorites = {

  food: ["mac and cheese", "steak", "salmon"], 
	
  activity: ["code", "walk", "play with dog", "sleep", "video games", "read"],
	
	show: ["Grey's Anatomy", "Twenties", "This is Us" ]
	
}

def hash_iteration(hash)
  hash.each do |x, y|
   puts "This is the main key: #{x} and the pairs:  #{y} that are a part of it."
  end
end


hash_iteration(celestes_favorites)
```

In the line ``` hash.each do |x,y| ```
x is defined as the hash KEYS and y is defined as the VALUES of those keys. So the above code would puts out 
```
This is the main key: food and the pairs:  ["mac and cheese", "steak", "salmon"] that are a part of it.
This is the main key: activity and the pairs:  ["code", "walk", "play with dog", "sleep", "video games", "read"] that are a part of it.
This is the main key: show and the pairs:  ["Grey's Anatomy", "Twenties", "This is Us"] that are a part of it.
```

But because hash.each is the last line being called it would return the entire hash celestes_favorites:

```
#=> {:food=>["mac and cheese", "steak", "salmon"], :activity=>["code", "walk", "play with dog", "sleep", "video games", "read"], :show=>["Grey's Anatomy", "Twenties", "This is Us"]}
```

This is the basics into hashes and understanding them as we get further along through the program I will learn more about what we can do with hashes and how to utilize them.





