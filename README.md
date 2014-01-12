KiUnit:  PaaS for the rest of us
================================

KiUnit is a PaaS offering for hobbyists to use.  It is (being) designed to be as simple as possible to setup and maintain for hobbyists running simple software (such as blog engines) on their own servers or VPS.  To that end, it relies on as few features as possible from the surrounding environment, and only provides the simplest of separation between components.  More centralized software components (like databases) are mostly assumed to be setup and managed by the user.

KiUnit is currently planned to cover the important PaaS pieces, including:
1. Simple Git push to deploy new version
2. Managing various resources from easy to use web interface (or the like).  Ideally this would be in the form of simple variables (eg. DB_CONNECT_STRING)
3. Automated process restart upon crashes.
4. Process separation through unix user/groups.

Eventually, KiUnit is meant to also support:
1. More complicated service startup (for now it is designed for http servers)
2. A custom http router to replace frontend web servers such as nginx or lighttpd.
3. Supporting other http services (such as fastcgi for php?)
4. Zero-down time upgrades, including the main KiUnit application.
5. Interesting and Magic dev/test/production separation.
6. Automated environment setup, for things like database, user/group, http server, dns, etc.