# Understanding CSS : Thinking inside the Box

Imagine that there is an invisible box around every HTML Element.

we've also seen the for each method which we can use in a race to find a callback function for each

item in the array.

So these are a few nice ways that we already have to cycle through arrays and do something with them.

But there's also several other methods that we can use on arrays as well.

On each of those methods does something different.

So in this chapter, I'm going to show you five array methods in total, and there are ways that we

can cycle through arrays and do something.

And the first one I'm going to show you is the filter method.

Now, before we start, notice, I've got an index dot hate mail page right here and it's linked up

to Sandbox Dot just now.

Over here, I have an array called Scores with different scores.

So then the array method filter.

When would I use this?

Well, I might use it if I retrieve some data from a database, for example, some scores and then this

array right here.

I want to filter out certain items from that array based on a certain condition.

So, for example, I might want to filter out all of the scores that are not at least 20 or that are

20 and over.

So I could do that using the filter method.

So what the filter method does is iterate an array and it performs a check on each item in the array

inside a callback function.

So this callback function finds for each item in the array perform some kind of check.

And if that check passes, then it's going to keep the item inside the filtered array.

If it doesn't pass, then it's going to filter out, it's going to remove it from the array.

So let's do a quick example.

What I'm going to do is take the scores array that we already have and use the dot filter method.

Now, I did say that this takes a callback function as an argument, so let's place that in here.

First of all, this is an arrow function.

And then inside here we have to return either true or false.

And if we return true, let me just correct the spelling that if we return true, then for that item

that we're currently iterating, we're going to keep that in the array.

If we return false, then we're not going to keep that in the array and we're going to filter out.

So let me just return true.

Here and explain what's going on.

So we're taking the scores, right?

And using the filter method, which fires a callback function for each item inside the array.

So currently when we start, it's going to be this item and what we're doing inside is returning.

True.

So that says, OK, well, keep this item in the array, then FISA callback function for the next item

again.

We return true in here.

So it keeps that item in the array, then the third we return.

True.

So it keeps that item and so forth.

And since we return, true in every case here, we're not actually filtering anything out of the array

because everything is going to stay in the array, because when we return, true, it keeps that item

in there right now.

If I was to change this to false, it would cycle through each item, perform the callback function

for each item and in each case return false.

And because we return false, then it's going to filter out each item.

So we're left with an empty array.

So we don't really want to do this return true or false like this, we want to return some kind of condition

that is going to evaluate to either true or false.

So, for example, if I want to filter out any score, which is not over 20, then what I do is return

score over twenty.

And obviously we need to take that score as a parameter here.

Now, this refers to the individual item each time we find the callback function.

So we take that score and we say, is he over 20 now?

If score is ten is ten over 20?

Well, this is going to evaluate to false and since we return, false.

Therefore we filter this item out, then we find the callback function for the next item and we have

30.

So now scores thirty.

Thirty over twenty.

Well, that's true.

So since it's true, we return true.

We keep that item in the array.

So what we're doing here is filtering out any number inside here or any score that is not over 20.

And then we should be left with just an array of scores which are over 20.

Now, this method, rather, this filter method, it's nondestructive.

And by that I mean it doesn't actually alter the original array.

So if I come down here and say console Decalogue and then try to log out the scores array, save it.

I'm going to preview over here.

I'm going to need to update my you are out to Chapter nine.

And if we see over here this array, it doesn't have any numbers filtered out of it because it's nondestructive.

This doesn't change the actual array, but we're trying to filter numbers out of it.

So how does this work?

Well, instead, what we do is we store the.

In a variable, so a contest and then say filtered scores, you can call this what you want and set

that equal to this method.

So what this does is now return a new array based on this criteria, based on what's kept in and what's

left out.

So if we save this now or in fact, we need to log out filtered scores here, save it, and now we should

see that filtered array.

So anything that's not over 20 is now not inside this.

Right.

So that's the basics of it.

But let's try something a bit more complex now.

So what I'm going to do is coming out of this dude and this one and come down underneath.

Now, what I'm going to do is create some data called uses and copying this from my Gilb repo because

I don't want to type out from scratch.

And all this is is an array and each item in the array is an object.

Each object has got a name property and a premium property.

So this premium property is going to be either true or false.

And it basically describes whether the user is a premium user or a premium member.

So, for example, Sean is a premium user because premium is set to true.

Yoshie Mario isn't, but Shonali is.

So what I'd like to do now is use the filter method to get an array of users who are premium users.

So I want to be left with ultimately Sean and Charnley.

But just imagine this was a huge array of hundreds of different users and we don't know which ones are

true or false.

We could use the same filter method that we're about to use to do something like this.

So this is a simplified version of it, but I'm going to say const and then premium users, because

we're storing this in a new constant or new variable because it's nondestructive.

It's not going to change this directly.

Then we take the users and we use the filter method inside the filter method.

We have a callback function on inside here.

This is where we return either true or false now that we want to take the individual user each time

around.

Now we're only going to take one parameter.

So let's delete the parentheses.

And we could have done that up here, by the way, but we didn't.

So let's do that again inside here.

We want to return either true or false.

Now we can return this property directly.

Each time around.

We can look on the individual user and the premium property because that is either true or false.

So if this is true, it's going to keep that user in the array.

If it's false, it's going to filter them out.

So now if I come down here and say console log and then premium, oops, premium users and save this,

then we should see an updated array with just two in it.

And it's just Sean and Shonali because they have the premium flag set to true.

Awesome.

Now just one thing, because we're just using a single return statement here and we did it here.

We're going to shorten this into a single line.

We can take away the curly braces and we can take away the return key word.

And then we just left with this.

So that is a nice, concise way to filter something out of an array and then get a new array based on

that.