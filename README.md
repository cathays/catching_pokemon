# Catching Pokemon
### Written by Louis Wain
### Methods Used
I've used two methods in which to query the API and handle the pagination. The first method I used
was to make requests in a loop until there were no more pages left. As long as `while url` was true,
I will make a request of the next page. This was a basic method and was the easiest way to handle this 
request I could think of.

The second method I used was similar, with one important difference. In the second method I chose to use
two packages called `aiohttp` and `nest_asyncio`. These two packages allow me to make requests
just like the `requests` package, but also allow me to do so asynchronously. This enables me to make
multiple requests at once and speed up the process. This can be really helpful when pulling
large amounts of data from an API. I used google to help me with this as I haven't used these
packages in a notebook before, and there is a slightly different method required when using these
in a notebook compared to a regular .py file. 


### Getting Abilities from 5 Pokemon
I chose to use the asynchronous version of this API call to take these 5 pokemon and their abilities. I chose
these 5 as they were the ones in my first team to beat Fire Red when I was younger. I've opted to hardcode 
the IDs in. I then loop through the list, adding the ID to the end of the API call and specifying which
parts of the data I want to return. The method is very similar to the previous API request,
it just has a `for` loop instead of a `while` loop.
