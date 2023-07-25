how to run
==========

<pre>
 ansible-rulebook -i inventory.yml --rulebook webhook.yml -v
 </pre>

 How to test
 ==========
 open other terminal and run 

 <pre>
 curl -H 'Content-Type: application/json' -d "{\"message\": \"Ansible is super cool\"}" 127.0.0.1:5000/endpoint
 </pre>
