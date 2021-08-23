
This webstack can be executed on a single node or multiple nodes. The inventory file
'hosts' defines the nodes in which the stacks should be configured.

        [webservers]
        localhost

The stack can be deployed using the following command:

        ansible-playbook -i hosts site.yml -vv   (for normal execution)
        ansible-playbook -i hosts site.yml --extra-vars="inputFile=input.yaml"   (for advanced execution where yaml is iterated using with_dict module in playbook kept inside roles/web/tasks/install_httpd.yml)

Once done, you can check the results by browsing to http://localhost/index.php.
You should see a simple test page..
