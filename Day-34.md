# Advanced Wordpressin'

## Custom Templating

You can define your own template items (beyond just header, footer, and sidebar) using the `get_template_part` function.

```php
<?php get_template_part( $slug, $name ); ?> 
```

### Examples

```php
<?php get_template_part( 'loop', 'index' ); ?>
//This will get the first file that exists among these, in this priority

//1. wp-content/themes/twentytenchild/loop-index.php
//2. wp-content/themes/twentyten/loop-index.php
//3. wp-content/themes/twentytenchild/loop.php
//4. wp-content/themes/twentyten/loop.php
```

```php
<?php get_template_part( 'nav' );           // Navigation bar (nav.php) ?>
<?php get_template_part( 'nav', '2' );      // Navigation bar #2 (nav-2.php) ?>
<?php get_template_part( 'nav', 'single' ); // Navigation bar to use in single pages (nav-single.php) ?>
```

## Post & Body Classes

What they're for

```css
.post {
	    /* styles for all posts */
}
.post-4564 {
	    /* styles for only post ID number 4564 */
}
.category-dancing {
	    /* styles for all posts within the category of dancing */
}
```

#### [Body Class](http://codex.wordpress.org/Function_Reference/body_class)

```php
<body <?php body_class($class); ?>> 
```

#### [Post Class](http://codex.wordpress.org/Function_Reference/post_class)

Only use this inside of the loop, as it applies to posts.

```php
<article id="post-<?php the_ID(); ?>" <?php post_class(); ?>>
```

## Javascript

Use wp_enqueue_script.

This is how your theme plays nicely with plugins when both need jQuery - we don't want jQuery to get loaded twice!


```php
<?php wp_enqueue_script( $handle, $src, $deps, $ver, $in_footer ); ?>
```




## [Custom Queries](http://codex.wordpress.org/Class_Reference/WP_Query)

```php
<?php 
// the query
$the_query = new WP_Query( $args ); ?>

<?php if ( $the_query->have_posts() ) : ?>

  <!-- pagination here -->

  <!-- the loop -->
  <?php while ( $the_query->have_posts() ) : $the_query->the_post(); ?>
    <h2><?php the_title(); ?></h2>
  <?php endwhile; ?>
  <!-- end of the loop -->

  <!-- pagination here -->

  <?php wp_reset_postdata(); ?>

<?php else:  ?>
  <p><?php _e( 'Sorry, no posts matched your criteria.' ); ?></p>
<?php endif; ?>
```

### Parameters

#### Author

```
author=1
author=3,5
author_name=matt_enlow
```

#### Category

```
cat=4
category_name=adventure_journal,photo_journal
```

#### Tags

```
tag=climbing,skiing //has any
tag=climbing+camping //has all
tag_id=13
```

#### So many, many others

Check out the nav menu on the codex wp_query section.
[http://codex.wordpress.org/Class_Reference/WP_Query](http://codex.wordpress.org/Class_Reference/WP_Query)


#### Params in action

```
$args = array(
    'tag' => 'skiing+climbing',
    'author_name' => 'matt_enlow'
);
$the_query = new WP_Query( $args ); ?>
```

### Reset your data!

After you're done using a custom query, reset everything back to the original, url based query via this function.

```php
<?php wp_reset_postdata(); ?>
```




# Guest Speaker: Brian Modena of [TMBR](http://wearetmbr.com)


Here is a quick outline - 
- I want to give a quick personal background
- Little info on TMBR
- Jump in to what we do / how we do it
- Give some advice for what employers want
- Open Forum Q/A


My Background
TMBR Elevator Pitch

What we do at TMBR - Technology 
- Web Development / branding / digital marketing
- Open Source
- Wordpress / laravel
- Jquery / angular
- HTML5 / CSS 3
- .git / .github
- grunt.js
- Mobile First
- UX / Ui Style boards / site boards
- Servers Hosting / Scalability - 

What Employers want
- Public code -  github / .bitbucket / codepen.io
- Start a personal site / Blog NOW !
- Cross train / learn design / SEO / Project Management
- Read industry blogs - Smashing / .net magazine / web design ledger
- Answer questions on stackoverflow

Being a good Freelancer :
- dont ever be late for anything ever
- Commit to what your good at
- Network every chance you get - silicon coulor / JH technolgst
- under charge and over deliver
- Work for / with good people - not every project is going to be a good fit - learn to quickly identify a bad one.

Open Q / A