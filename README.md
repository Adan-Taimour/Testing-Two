bench start
bench new-site print-designer.test
bench --site print-designer.test add-to-hosts
bench get-app https://github.com/frappe/print_designer
bench --site print-designer.test install-app print_designer
 
//Check Installed App List
bench --site site1.local list-apps
 
--------------------
IF Not Working
--------------------
 
bench --site site1.local clear-cache
bench --site site1.local clear-website-cache
bench --site site1.local reload-doc print_designer
bench --site site1.local migrate
 
bench --site site1.local list-apps
 
----------------
//If Not Working..........
----------------
 
//Uninstall the App:
bench --site site1.local uninstall-app print_designer
 
//Reinstall the App:......
bench --site site1.local install-app print_designer
 
//Restart Supervisor......
sudo supervisorctl restart all
 
 
 
Restart Your Computer.........
