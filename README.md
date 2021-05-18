UPDATE wp_options SET option_value = REPLACE(option_value, 'https://ploshadka.net', 'http://localhost:8888/ploshadka.net') WHERE option_name = 'home' OR option_name = 'siteurl';

UPDATE wp_posts SET post_content = REPLACE (post_content, 'https://ploshadka.net', 'http://localhost:8888/ploshadka.net');

UPDATE wp_postmeta SET meta_value = REPLACE (meta_value, 'https://ploshadka.net', 'http://localhost:8888/ploshadka.net');

UPDATE wp_posts SET guid = REPLACE (guid, 'https://ploshadka.net', 'http://localhost:8888/ploshadka.net') WHERE post_type = 'attachment';
