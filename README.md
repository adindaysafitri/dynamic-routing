<h1>Dynamic Routing Protocol Simulation using Docker</h1>
<h2>Description</h2>
<p>This project simulates dynamic routing in a network environment using Docker and FRRouting (FRR). 
  It is designed to provide hands-on experience with routing protocols and network configuration.</p>
    <h2>Environment</h2>
    <ul>
        <li><strong>Virtualization:</strong> Docker and Docker Compose.</li>
        <li><strong>Routing tool:</strong> FRRouting (FRR), A suite of network protocols used to manage dynamic routing.</li>
        <li><strong>Operating systems:</strong> Uses Ubuntu 22.04 as the base image operating system for router.
            <ol type="a">
              <li>Uses Ubuntu 22.04 as the base image operating system for routers.</li>
              <li>Uses Alpine Linux as the base image operating system for PCs.</li>
            </ol>
        </li>
        <li><strong>VTYSH:</strong> A shell interface for managing FRRouting on the router.</li>
        <li><strong>Bash:</strong> Shell for the PC.</li>
    </ul>
    <h2>Preparation Steps</h2>
    <p>Run the following commands to create Docker networks:</p>
    <pre>
docker network create --subnet 192.168.10.0/24 lan1
docker network create --subnet 192.168.20.0/24 lan2
docker network create --subnet 192.168.30.0/24 lan3
docker network create --subnet 192.168.40.0/29 link1
docker network create --subnet 192.168.50.0/29 link2 </pre>
    <h2>Usage</h2>
    <ol>
        <li><strong>Build the image:</strong>
            <pre>docker-compose build</pre>
        </li>
        <li><strong>Run the containers:</strong>
            <pre>docker-compose up -d</pre>
        </li>
        <li><strong>Access the shell:</strong>
            <ul>
                <li><strong>Router:</strong>
                    <pre>docker exec -it &lt;router-cont&gt; vtysh</pre>
                </li>
                <li><strong>PC:</strong>
                    <pre>docker exec -it &lt;pc-cont&gt; bash</pre>
                </li>
            </ul>
        </li>
      </ol>
      <h2>Features</h2>
        <ul>
          <li>Simulates dynamic routing protocols in a containerized environment.</li>
          <li>Easy setup using Docker Compose.</li>
          <li>Lightweight PC nodes using Alpine Linux.</li>
        </ul>
