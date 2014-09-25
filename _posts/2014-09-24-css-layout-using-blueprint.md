---
layout: post
title: CSS Layout using Blueprint
---

You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve --watch`, which launches a web server and auto-regenerates your site when a file is updated.

To add new posts, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext` and includes the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight css %}
.icon {
    display: inline-block;
    width:  16px;
    height: 16px;
    background-image: url(/img/sprite.svg);
}

.icon--home     { background-position:   0     0  ; }
.icon--person   { background-position: -16px   0  ; }
.icon--files    { background-position:   0   -16px; }
.icon--settings { background-position: -16px -16px; }
{% endhighlight %}

{% highlight javascript %}
var person = {
    fname: "John",
    lname: "Doe",
    age: "40",
    fullname: function () {
        return this.fname + " " + this.lname;
    }
};
console.log(person.fullname());
{% endhighlight %}


{% highlight javascript %}
function Mammal(name) {
    this.name = name;
    this.offspring = [];
}
Mammal.prototype.haveABaby = function () {
    var newBaby = new Mammal("Baby " + this.name);
    this.offspring.push(newBaby);
    return newBaby;
}
Mammal.prototype.toString = function () {
    return '[Mammal "' + this.name + '"]';
}
Cat.prototype = new Mammal(); // Here's where the inheritance occurs
Cat.prototype.constructor = Cat; // Otherwise instances of Cat would have a constructor of Mammal, creates an object of Cat.

function Cat(name) {
    this.name = name;
}
Cat.prototype.toString = function () {
    return '[Cat "' + this.name + '"]';
}
var someAnimal = new Mammal('Mr. Biggles');
var myPet = new Cat('Felix');
alert('someAnimal is ' + someAnimal); // results in 'someAnimal is [Mammal "Mr. Biggles"]'
alert('myPet is ' + myPet); // results in 'myPet is [Cat "Felix"]'
myPet.haveABaby(); // calls a method inherited from Mammal
alert(myPet.offspring.length); // shows that the cat has one baby now
alert(myPet.offspring[0]); // results in '[Mammal "Baby Felix"]'
{% endhighlight %}

Check out the [Jekyll docs][jekyll] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll’s dedicated Help repository][jekyll-help].

[jekyll]:      http://jekyllrb.com
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-help]: https://github.com/jekyll/jekyll-help
