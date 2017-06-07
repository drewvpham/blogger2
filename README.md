# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

1.upto(5) {|i| Blog.create(name:"blogname#{i}, description:"description#{1}")}
Owner.create(user: User.first, blog: Blog.first)
Owner.create(user: User.first, blog: Blog.second)
Owner.create(user: User.first, blog: Blog.third)
Blog.find(4).owner(Owner.second)
Owner.create(user:User.second, blog:Blog.fourth)
Owner.create(user:User.last, blog:Blog.fifth)
Blog.all.each{|blog| Owner.create(user:User.third, blog:blog)}
