..
  Warning: Do not edit this file. It is automatically generated and your
  changes will be overwritten. The tool to do so lives in the
  openstack-doc-tools repository.

.. list-table:: Description of configuration options for ``[container-replicator]`` in ``container-server.conf``
   :header-rows: 1
   :class: config-ref-table

   * - Configuration option = Default value
     - Description
   * - ``concurrency`` = ``8``
     - Number of replication workers to spawn
   * - ``conn_timeout`` = ``0.5``
     - Connection timeout to external services
   * - ``interval`` = ``30``
     - Minimum time for a pass to take
   * - ``log_address`` = ``/dev/log``
     - Location where syslog sends the logs to
   * - ``log_facility`` = ``LOG_LOCAL0``
     - Syslog log facility
   * - ``log_level`` = ``INFO``
     - Logging level
   * - ``log_name`` = ``container-replicator``
     - Label used when logging
   * - ``max_diffs`` = ``100``
     - Caps how long the replicator spends trying to sync a database per pass
   * - ``node_timeout`` = ``10``
     - Request timeout to external services
   * - ``per_diff`` = ``1000``
     - Limit number of items to get per diff
   * - ``reclaim_age`` = ``604800``
     - Time elapsed in seconds before an object can be reclaimed
   * - ``recon_cache_path`` = ``/var/cache/swift``
     - Directory where stats for a few items will be stored
   * - ``rsync_compress`` = ``no``
     - Allow rsync to compress data which is transmitted to destination node during sync. However, this is applicable only when destination node is in a different region than the local one.
   * - ``rsync_module`` = ``{replication_ip}::container``
     - Format of the rsync module where the replicator will send data. The configuration value can include some variables that will be extracted from the ring. Variables must follow the format {NAME} where NAME is one of: ip, port, replication_ip, replication_port, region, zone, device, meta. See etc/rsyncd.conf-sample for some examples. uses what's set here, or what's set in the DEFAULT section, or 10 (though other sections use 3 as the final default).
   * - ``run_pause`` = ``30``
     - Time in seconds to wait between replication passes
