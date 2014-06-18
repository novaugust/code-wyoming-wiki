![](http://codex.wordpress.org/images/1/18/Template_Hierarchy.png)


#[Function Reference](http://codex.wordpress.org/Function_Reference)


# Templating Functions


* `get_header()` for `header.php`
* `get_sidebar()` for `sidebar.php`
* `get_footer()` for `footer.php`


## Plugin Hooks

* `wp_head()`
* `wp_footer()`
* `wp_meta()`


## Escape Attributes

`esc_attr()`
`the_title_attribute()`

# Getting User Values

wp_title    

### wp_nav_menu

* `container` ('div')
* `container_class`
* `container_id`
* `menu_class`
* `menu_id`

##### Multiple Menus

`theme_location($slug)`
[`register_nav_menu($slug, $user_friendly_description)`](http://codex.wordpress.org/Function_Reference/register_nav_menu) (functions.php)


# The Loop

```php
<?php if ( have_posts() ) : while ( have_posts() ) : the_post(); ?>
<!-- loop it up! -->
<?php endwhile; else: ?>
<p>Sorry, no posts matched your criteria.</p>
<?php endif; ?>
```

## Inside the loop

See [template tags](http://codex.wordpress.org/Template_Tags) for the full documentation on what you can do in The Loop.

### Title, Date, Author, & Post Link


* `the_permalink()`
* `the_title()` or `the_title('before', 'after')`
* `the_title_attribute()`
* [`the_time()`](http://codex.wordpress.org/Function_Reference/the_time)
* `the_author()`

```php
<h2 id="post-<?php the_ID(); ?>">
<a href="<?php the_permalink() ?>" rel="bookmark" title="Permanent Link to <?php the_title_attribute(); ?>">
<?php the_title(); ?></a></h2>
<small><?php the_time('F jS, Y') ?> <!-- by <?php the_author() ?> --></small>
```

### Post Tags

```php
<?php the_tags( $before, $sep, $after ); ?> 
```


### Post Body

#### The Content

* `the_content('Read more link text')`

```php
<?php the_content("Continue reading " . the_title('', '', false)); ?>
```

#### The Excerpt
Strips HTML (including imgs) and cuts down to 55 words. No readmore link.



#### <!--More--> : Content vs Excerpt

```php
<?php if ( is_category() || is_archive() ) {
	the_excerpt();
} else {
	the_content();
} ?>
```


## [Pagination](http://codex.wordpress.org/Pagination)



```php
<?php if ( have_posts() ) : ?>

<!-- Add the pagination functions here. -->

<!-- Start of the main loop. -->
<?php while ( have_posts() ) : the_post();  ?>

<!-- the rest of your theme's main loop -->

<?php endwhile; ?>
<!-- End of the main loop -->

<!-- Add the pagination functions here. -->

<div class="nav-previous alignleft"><?php next_posts_link( 'Older posts' ); ?></div>
<div class="nav-next alignright"><?php previous_posts_link( 'Newer posts' ); ?></div>

<?php else : ?>
<p><?php _e('Sorry, no posts matched your criteria.'); ?></p>
<?php endif; ?>
```




# Frameworks

* [_s, 'underscores'](http://underscores.me/) and here's an [intro to underscores](http://wptavern.com/introduction-to-underscores-a-wordpress-starter-theme-with-konstantin-obenland)
* [roots](http://roots.io/starter-theme/)
    
    ps: check out the "recommended plugins" at the bottom of roots!
    
* [bones](http://themble.com/bones/) minimal, less frameworky