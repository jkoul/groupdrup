# groupdrup
9/11 Drupal Teach-Yourself Project

Example of basic Drupal website (using Acquia):<br />
http://wdidrupalpykfbrdyks.devcloud.acquia-sites.com/node/1


<p>**Project Participants**:<br />
Tom Beach <br />
Jeremy Koulish<p>

**Overview**
<p>A first look at Drupal tutorial sites suggests that we might be stepping back into "old school" land.  High word density, traditional layouts, lack of design originality are not exactly enticing.  However, Drupal is one of the workhorse technologies for the federal government, and Drupal skills are in high demand.  Though it may appear old school by look and feel, it is most au courant for job seekers in Washington DC.<p>

<p>**Getting Started**</p>

<p>A quick review of getting started websites led to the distinction between core and distribution installations.  Core installations involve a "steep learning curve" according to some web authors, whereas distributions come pre-configured for specific user needs.  Business front-end, community resource, and conference organizing are a few of the options.  Thinking we were about to set up a "manageable" site to serve via local computer, we went with the community resource "Drupal Commons", then chose to pursue a core-driven solution using the MAMP (Mac, Apache, MySQL, PHP) server stack.</p>


**Drupal Installation Instructions**<br />
See https://www.drupal.org/documentation/install/ for more detailed instructions.

1. Install Drupal via command line
  - install composer:

  ```
  curl -sS https://getcomposer.org/installer | php
  mv composer.phar /usr/local/bin/composer
  ```

  - install drush:

  ```
  composer global require drush/drush:7.*
  ```
  - restart bash, then install drupal:

  ```
  drush dl drupal

  ```

2. Install MAMP:
  - https://www.mamp.info/en/downloads/
  - Click "Download" and follow installation instructions
  - open using MAMP Pro (free trial)

3. Configure Drupal settings
  - duplicate the default.settings.php file and rename the copy as settings.php.  
  From within your main drupal folder:
  ```
  cp sites/default/default.settings.php sites/default/settings.php
  ```
  - Change key files to allow editing during install:
  ```
  chmod a+w sites/default/settings.php
  ```
  ```
  chmod a+w sites/default
  ```

4. Move Drupal files into MAMP application:
  ```
  mv drupal-x.x.x/* drupal-x.x.x/.htaccess /Applications/MAMP/htdocs/yourdrupaldir
  ```
  where yourdrupaldir is whatever you want the directory to be called and "drupal-x.x.x" should match the version of Drupal you just installed.


5. Create Drupal database using MySQL
  - Follow instructions in the "Create the Drupal database" section of:
  https://www.drupal.org/node/66187

6. Run the Drupal installation script
  - Go to http://localhost:8888/yourdrupaldir/install.php and follow the prompts.
  Note: The name of "yourdrupaldir" in that URL should match the one you use in Step 4.

7. Customize your new Drupal site!
