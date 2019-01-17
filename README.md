tds_fdw
=======

CentOS/RH/Amazon RPMs for tds_fdw  <https://github.com/GeoffMontee/tds_fdw> and postgresql 9.3.4 or later

Tested on CentOS 6/7 x86_64. Should work for other RPM base distributions such as openSUSE or Amazon Linux

tds_fdw is a PostgreSQL foreign data wrapper that can connect to databases that use the Tabular Data Stream (TDS) protocol, such as Sybase databases and Microsoft SQL server.

It does not yet support write operations, as added in PostgreSQL 9.3.

PostgreSQL versions that the SPEC can support
---------------------------------------------
* 9.3 >= 9.3.4 (EoL and not maintained by tds_fdw upstream anymore)
* 9.4 >= 9.4.1
* 9.5 >= 9.5.1
* 9.6 >= 9.6.1
* 10 >= 10.0

Requirements
------------

To build: 

* freetds-devel
* gcc
* Git
* make
* rpmbuild

And:

* postgresql[version]-devel

Being **[version]** one of: 93, 94, 95, 96 or 10

To install the RPM for PostgreSQL

* freetds >= 0.91

And:
* postgresql[version]
* postgresql[version]-server
* postgresql[version]-libs

Being **[version]** one of: 93, 94, 95, 96 or 10

Building fresh RPMs
-------------------

Clone the repo: 

    git@github.com:juliogonzalez/tds_fdw-rpm.git
    cd tds_fdw-rpm


Build the tds_fdw RPM
---------------------

Build the RPMs for with:

    ./tds-fdw_rpm -p [version]

Where `[version]` is one of: 9.3, 9.4, 9.5, 9.6 or 10

And install with

    rpm -Uvh RPMS/$HOSTTYPE/postgresql-[version]-tds_fdw-*.*.$HOSTTYPE.rpm

Where `[version]` is one of: 9.3, 9.4, 9.5, 9.6 or 10
