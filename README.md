Role Name
=========

> Red Hat systems require registration to access content updates.

Register systems with either CDN or satellite.

Requirements
------------

 If using satellite, activation keys or credentials should be created.
 If registering directly to Red Hat CDN, credentials or activation keys should be created.

Role Variables
--------------

Available variables are listed below, along with default values (see defaults/main.yml):

    # Platform you wish to deploy a Cornerstone VM onto
    rh_username:
    rh_password:
    
    # Requires that the activation key be precreated. 
    rh_ak:

    # This can be found in your Red Hat online portal.
    # Or if using satellite this will be in the Organizations section. 
    # First organization is normally 1
    rh_orgid:

    # Currently supports yes or no
    rh_forceregister:

    # Satellite server variables
    # currently accepts yes and no
    rh_usesat: no
    rh_satserver:
    # Default value is set for this but useful if anything changes with satellite.
    rh_satserver_rpm_path: pub
    # Name of the RPM file that will be used to install satellite certificates and 
    # configuration required for satellite client registration. Default valu
    rh_rpmname: katello-ca-consumer-latest.noarch.rpm 

Future Releases
---------------

 - Add support for more options in the register module using templates.

License
-------

MIT

Author Information
------------------

Ken Hitchcock [Github](https://github.com/kenhitchcock)

