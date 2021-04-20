<!-- wp:heading {"level":3} -->
<h3>Bind mounts</h3>
<!-- /wp:heading -->

<!-- wp:list -->
<ul><li>Bind mounts can be stored anywhere on the host system. It is available since the early days of docker. </li></ul>
<!-- /wp:list -->

<!-- wp:list -->
<ul><li>When we use a bind mount, a directory or file on the host machine is mounted into the container. </li></ul>
<!-- /wp:list -->

<!-- wp:list -->
<ul><li>Basically, we use bind mount when we need to use a file or directory of our host machine inside the container.</li></ul>
<!-- /wp:list -->

<!-- wp:list -->
<ul><li>To use bind mount the absolute path is given as mount point.<br>Non-docker processes or docker processes can also modify these files or data any time since this is data in host filesystem.</li></ul>
<!-- /wp:list -->

<!-- wp:list -->
<ul><li>As bind mounts are not existed in docker, so we can not manage them using docker CLI commands.</li></ul>
<!-- /wp:list -->

<!-- wp:heading {"level":3} -->
<h3>Tmpfs mount</h3>
<!-- /wp:heading -->

<!-- wp:list -->
<ul><li>A tmpfs mount does not exist on the disk or host file system. It is stored in the host memory.</li><li>Whenever, we restart or stop our container the data is lost.</li><li>So, tmpfs is non persistent file system which is used in some specail cases.</li><li>It can be used by container till it is running. As soon as we stop the container the data is not be used again as it is removed immediately.</li><li>We can use tmpfs to store sensitive data which is not needed for future use.</li><li>One more use of tmpfs is that, docker swarm use tmpfs mount point internally to interact between several containers. </li></ul>
<!-- /wp:list -->
