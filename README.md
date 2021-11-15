# Coding-Standard
Coding Standard PHPCS and PHPCBF

**Drupal – Check**
------------------

    Firstly Download the new project using link below:-
      1. composer create-project drupal-composer/drupal-project:8.x-dev drupal_depricated --no-interaction --stability=dev
    
   follow this way no need to setup the manually, and remember the to change the drupal version you want or project name.
    
    https://github.com/mglaman/drupal-check
    
  You can also install this globally using Composer like so:
  first of all run the command on git bash root directory:-
    
    composer global require mglaman/drupal-check
    
   and,
   
    run drupal-check drupal/path/to/contrib/my_modulename
    * * drupal-check -a drupal/path/to/contrib/my_modulename
    
   Analysis the module not check the deprication.
   
    ** drupal-check -d drupal/path/to/contrib/my_modulename
    
   Deprication check
   
    ** drupal-check -ad drupal/path/to/contrib/my_modulename
    
   Both Analysis and deprication
  ------------------------------------------------------------------------------------------------------------ 
  
 **  Drupal codesniffer with phpcs**
 ----------------------------------
    https://www.drupal.org/docs/contributed-modules/code-review-module/installing-coder-sniffer
    
  it check the line indentation, backspace and whitespaces etc.
  it first need to install drupal/coder
  run command on CLI
    
    composer global require drupal/coder:^8.3.1
    composer global require dealerdirect/phpcodesniffer-composer-installer
    
   1. Now, installation is done, then run the command to check Error:
   
    phpcs --standard=Drupal --extensions=php,module,inc,install,test,profile,theme,css,info,txt,md,yml /path/to/drupal/example_module
    
 ----------------------------------------------------------------------------------------------------------
 
 ** Drupal – Check
 -----------------
    **Red color indicates to mention here your project/file path..!!
    
   2. after phpcs command done, then run the automatically fix coding standard command
   
    phpcbf --standard=Drupal --extensions=php,module,inc,install,test,profile,theme,css,info,txt,md,yml /path/to/drupal/example_module
    
   **Red color indicates to mention here your project/file path..!!
   
 -------------------------------------------------------------------------------------------------------------
 
 ** Drupal Practice
 ------------------
 Drupal Practice alwaysrun with phpcs because it show the dependency error and warnings.
 
     phpcs --standard=DrupalPractice --extensions=php,module,inc,install,test,profile,theme,css,info,txt,md,yml /path/to/drupal/example_module
     
Remember:-
Drupal Practice can’t be run with phpcbf, because phpcbf can’t be fixed bug related to
dependency error..

-------------------------------------------------------------------------------------------------------------------

PHPCS and PHPCBF global

    composer global require drupal/coder dealerdirect/phpcodesniffer-composer-installer
