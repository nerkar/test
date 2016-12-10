find   -iname '*.html'

find all .html

find   -iname 'index.html' | wc -l 

find   -iname '*.xml' | wc -l 


 // find location url in .xml file
grep -n "loc" sitemap.xml | wc -l

// combine both above command for single result which find all the .xml files in the entire directory-tree and perform grep for each .xml file returned.




find   -iname 'sitemap.xml'  -exec grep   -n   "loc" {} \+| wc -l



// prepend text to each line 
  awk '{print "Redirect 301  " $0;}' r1.txt > output.txt





// concat two files linve by line
paste file1.txt file2.txt > output.txt


// add  end of each line  (\/) '/' is added in each line 

sed 's/$/\//' r1.txt >  sc.txt

-----------

rsync directory


rsync -avz /dirname  praveen@192.168.1.114:/destination/dir/location

--- delete a branch in git

 git push origin --delete <branch_name>

example

git push origin --delete feature-new-server-config


> print / delete alternative line
(to print odd lines)
sed -n 1~2p output1.txt > third.txt

(print even number lines)
sed -n 2~2p output1.txt > third.txt





--wifi configuration
> connect to wifi 
nmcli c up  JIO_ICT_1


> turn wifi on 
nmcli radio wifi on

> list of wired connection
nmcli c

> list of saved wifi connections

nmcli d wifi list

-----
enabling - disabling service in ubuntu

link : http://askubuntu.com/questions/19320/how-to-enable-or-disable-services

command :
systemctl enable <service-name>
> check service is enabled or not 
systemctl is-enabled <service-name>



-> extract url's from text file
cat old.xml  | grep http | grep -shoP 'http.*?[" >]' >  out-old.xml


-> extract filename from the url or path from text file
sed 's@.*/@@'  test.xml


## connect to available wifi using terminal 
 sudo nmcli dev wifi connect ICT password 002062623

