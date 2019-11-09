# L6Modular Modified by Gm Omar Farook Hridoy
This package gives you the ability to use Laravel 6 with module system. You can simply drop or generate modules with their own controllers, models, views, translations and a routes file into the <code>app/Modules</code> folder and go on working with them.
# Attention
"This package originally created by artem-schander", I just modified some code and implement for <code>Laravel 6</code>. Thanks.

# Dcumentation
<ul>
<li>Installation</li>
<li>Getting started</li>
<li>Usage</li>
</ul>

# Istallation
The best way to install this package is through your terminal via Composer.<br>

Run the following command from your projects root

<code>composer require devhridoy/l6modular</code> 

Once this operation is complete, simply add the service provider to your project's config/app.php and you're done.

# Service Provider

<code>Devhridoy\L6modular\ModuleServiceProvider::class</code> 

# Setting Started
<p>The built in Artisan command <code>php artisan make:module name [--no-migration] [--no-translation]</code> generates a ready to use module in the <code>app/Modules</code> folder and a migration/translation if necessary.</p>

<p>Since version 1.3.0 you can generate modules named with more than one word, like <code>foo-bar</code>.</p>

<p>This is how the generated module would look like:</p>
<pre><code>laravel-project/
    app/
    └── Modules/
        └── FooBar/
            ├── Controllers/
            │   └── FooBarController.php
            ├── Models/
            │   └── FooBar.php
            ├── Views/
            │   └── index.blade.php
            ├── Translations/
            │   └── en/
            │       └── example.php
            ├── routes
            │   ├── api.php
            │   └── web.php
            └── helper.php
                
</code></pre>

# Usage
<p>The generated <code>RESTful Resource Controller</code> and the corresponding <code>routes/web.php</code> make it easy to dive in. In my example you would see the output from the <code>Modules/FooBar/Views/index.blade.php</code> by opening <code>laravel-project:8000/foo-bar</code> in your browser.</p>

# Update 1.0.0 For Laravel 6

<p>You have to follow the <code>upper camel case</code> name convention for the module folder. If you had a <code>Modules/foo</code> folder you have to rename it to <code>Modules/Foo</code>.</p>

<p>Also there are changes in the <code>app/config/modules.php</code> file. Now you have to return an array with the key <code>enable</code> instead of <code>list</code>.</p>

# License
<p>L6 Modular is licensed under the terms of the <a href="http://opensource.org/licenses/MIT" rel="nofollow">MIT License</a>
(See LICENSE file for details).</p>
