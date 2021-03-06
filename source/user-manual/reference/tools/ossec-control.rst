
.. _ossec-control:

ossec-control
=============

The ossec-control script is used to start, stop, configure, or check on the status of Wazuh processes.  This script can enable or disable client-syslog, database logging, agentless configurations, integration with slack and pagerduty, and debug mode.

+-------------+---------------------------------------------------------------------------------------------------------+
| **start**   | Start the Wazuh processes.                                                                              |
+-------------+---------------------------------------------------------------------------------------------------------+
| **stop**    | Stop the Wazuh processes.                                                                               |
+-------------+---------------------------------------------------------------------------------------------------------+
| **restart** | Restart the Wazuh processes.                                                                            |
+-------------+---------------------------------------------------------------------------------------------------------+
| **reload**  | Restart all Wazuh processes except ossec-execd.                                                         |
|             |                                                                                                         |
|             | This allows an agent to reload without losing active response status.                                   |
|             |                                                                                                         |
|             | This option is not available on a local Wazuh installation.                                             |
+-------------+---------------------------------------------------------------------------------------------------------+
| **status**  | Determine which Wazuh processes are running.                                                            |
+-------------+---------------------------------------------------------------------------------------------------------+
| **enable**  | Enable Wazuh functionality.                                                                             |
+             +-----------------+---------------+-----------------------------------------------------------------------+
|             | Allowed options | database      | Enable the ossec-dbd daemon for logging to a database.                |
+             +                 +               +-----------------------------------------------------------------------+
|             |                 |               | Server and local                                                      |
+             +                 +---------------+-----------------------------------------------------------------------+
|             |                 | client-syslog | Enable ossec-csyslogd for logging to remote syslog.                   |
+             +                 +               +-----------------------------------------------------------------------+
|             |                 |               | Server and local                                                      |
+             +                 +---------------+-----------------------------------------------------------------------+
|             |                 | agentless     | Enable ossec-agentlessd for running commands on systems               |
|             |                 |               |                                                                       |
|             |                 |               | without Wazuh agents.                                                 |
+             +                 +               +-----------------------------------------------------------------------+
|             |                 |               | Server and local                                                      |
+             +                 +---------------+-----------------------------------------------------------------------+
|             |                 | integrator    | Enable integrator for connection to external APIs and alerting tools. |
+             +                 +               +-----------------------------------------------------------------------+
|             |                 |               | Server                                                                |
+             +                 +---------------+-----------------------------------------------------------------------+
|             |                 | auth          | Enable the ossec-authd daemon for add agents to the manager.          |
+             +                 +               +-----------------------------------------------------------------------+
|             |                 |               | Server                                                                |
+             +                 +---------------+-----------------------------------------------------------------------+
|             |                 | debug         | Run all Wazuh daemons in debug mode.                                  |
+-------------+-----------------+---------------+-----------------------------------------------------------------------+
| **disable** | Disable Wazuh functionality.                                                                            |
+             +-----------------+---------------+-----------------------------------------------------------------------+
|             | Allowed options | database      | Disable the ossec-dbd daemon for logging to a database.               |
+             +                 +               +-----------------------------------------------------------------------+
|             |                 |               | Server and local                                                      |
+             +                 +---------------+-----------------------------------------------------------------------+
|             |                 | client-syslog | Disable ossec-csyslogd for logging to remote syslog.                  |
+             +                 +               +-----------------------------------------------------------------------+
|             |                 |               | Server and local                                                      |
+             +                 +---------------+-----------------------------------------------------------------------+
|             |                 | agentless     | Disable ossec-agentlessd for running commands on systems              |
|             |                 |               |                                                                       |
|             |                 |               | without Wazuh agents.                                                 |
+             +                 +               +-----------------------------------------------------------------------+
|             |                 |               | Server and local                                                      |
+             +                 +---------------+-----------------------------------------------------------------------+
|             |                 | integrator    | Disable integrator for connection to external APIs and alerting tools.|
+             +                 +               +-----------------------------------------------------------------------+
|             |                 |               | Server                                                                |
+             +                 +---------------+-----------------------------------------------------------------------+
|             |                 | auth          | Enable the ossec-authd daemon for add agents to the manager.          |
+             +                 +               +-----------------------------------------------------------------------+
|             |                 |               | Server                                                                |
+             +                 +---------------+-----------------------------------------------------------------------+
|             |                 | debug         | Turn off debug mode.                                                  |
+-------------+-----------------+---------------+-----------------------------------------------------------------------+

.. note::
    To use the database option, Database support must be compiled in during initial installation.
