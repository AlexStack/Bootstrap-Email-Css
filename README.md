# Why need bootstrap email css?
- The original bootstrap.min.css is a little too big for inline email css
- This short version of bootstrap email css is less than 60KB

# How to use it in email template?
```html
<html>
<head>
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
    <title>Bootstrap email css template example</title>
        <style media="all" type="text/css">
        [COPY THE MINIFIED CSS CODE (eg. from bootstrap4-email-css.min.css) INSERT IT HERE. YOU *CANNOT* JUST USE A CSS REFERENCE.]
    </style>
</head>
<body>
<div class="container">
    <div class="row justify-content-center">
        <div class="col-md-11">
                <div class="card p-2 mb-3">

                    <div class="border-t-2 w-100  mb-3 pt-3 text-dark">    
                        {!! $email-content !!}
                    </div> 

                </div>
        </div>
    </div>
</div>
</body>
</html>
```

# What can we use?
- I removed the barely used feature in email, eg. form, input, table, modal, dropdown, nav, navbar, carousel, tooltips
- Other features are available, eg. col-x, col-md-x