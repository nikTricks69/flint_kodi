# flint_kodi
attached my movies to flint 2 router and had a hard time getting Kodi to read ,after some debugging and forums I have it working so thought of scribbling it here,may help someone

# Enable WebDav in Flint 2
 Follow the wiki https://docs.gl-inet.com/router/en/4/interface_guide/network_storage/#set-up-webdav
 Create a user
 and allow webdav via WAN and I also chose HTTPS
 Its important to note that it uses a self signed cert that Kodi doesnt understand
 Also note that if you test the endpoint via browser you will get a 403 forbidden , better test using something like CX explorer
# setup Kodi
 Setup a new networka and choose WebDAV (Https)
 URL be like davs://console.gl-inet.com:6008/disk1_part1/1my%20downloads/|verifypeer=false
Notes:
  console.gl-inet.com is the CN of the self signed cert , IP didnt work for me
  %20 instead of space 
  |verifypeer=false tells Kodi to ignore the certificate verification


  I also had to restart Kodi to get things to work and pretty impressed , much faster and smooth in comparison to my old NFS setup 

  Trouble Shooting
  check 
  mediasources.xml
  sources.xml
  and enable logging in Kodi if needed 

  Hope this helps someone, enjoy :)
