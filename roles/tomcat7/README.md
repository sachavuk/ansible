# Ansible Role: Tomcat 7

An Ansible Role that installs Tomcat 7 on CentOS 6.x and Debian 7.x.

## Requirements

Java may be ;)

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    tomcat_tgz_url: url to download tomcat
    tomcat_tgz: name of the file tar.gz
    tomcat_dir: name of directory after extraction

You can specified another value for this variables in your inventory file , the default value from `defaults/main.yml` will be overwrite
   
    user_tomcat: Specified an user who will run tomcat, default root
    product_dir: Specified path directory for you tomcat projects ( example: /home/produits/apirest)
    product_name: Specified name of project (example: apirest)
    JAVA_OPTS: Specified options for tomcat, example memory size for tomcat.. optional  
    http_shutdown: tomcat shutdown port default value 8005
    tomcat_address: tomcat listen addresse default value 127.0.0.1
    http_tomcat: Tomcat http port for connector http default value 8080
    ajp_tomcat: Tomcat ajp port for connector ajp default value 8009
    tomcat_classpath: Specified a classpath for tomcat load jar files, optional
    

## Dependencies

None

## Example Playbook

    - hosts: tomcatservers
      roles:
        - { role: tomcat7 }


