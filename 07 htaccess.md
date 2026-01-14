********************************************************************************
# Document 07 -- htaccess.md (Security Configuration)
Rev 1.0.0 - Original Issue
********************************************************************************

***

## Security Configuration Rules

### Executable Code (Apache .htaccess)

# --- SECURITY RULES ---
# Define a plain-text error message to avoid the ErrorDocument 403 loop
ErrorDocument 403 "Access Denied: Path not authorized."

# Allow public access to robots.txt to ensure crawler compliance
# This bypasses global directory authentication for this specific file.
<Files "robots.txt">
    Satisfy Any
    Allow from all
</Files>

RewriteEngine On

# Content Integrity Rule: White-list approach
# Only allows access to the root, sitemap, robots, and specific core files.
# All other requests outside the /monsantobeach/ directory are forbidden (403).
RewriteCond %{REQUEST_URI} !^/($|sitemap\.xml|robots\.txt|index\.html|info\.php|favicon.*|monsantobeach/) [NC]
RewriteRule ^ - [F,L]

# Deny access to hidden files (starting with a dot)
<FilesMatch "^\.\">
    Require all denied
</FilesMatch>

# --- PHP HANDLER (DO NOT EDIT) ---
# Set the “ea-php84” package as the default “PHP” programming language.
<IfModule mime_module>
  AddHandler application/x-httpd-ea-php84___lsphp .php .php8 .phtml
</IfModule>

# Logging & Audit
# Verification of T=0 is confirmed by a Status 200 response for /robots.txt.

***

********************************************************************************
End of Document 07 -- htaccess.md (Security Configuration)
This file is complete and has not been truncated.
********************************************************************************