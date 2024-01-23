# SFB 1451 superdataset

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.10556115.svg)](https://doi.org/10.5281/zenodo.10556115)

This repository is a [DataLad](https://www.datalad.org/) dataset. It
provides fine-grained data access down to the level of individual
files, and allows for tracking future updates. In order to use this
repository for data retrieval, [DataLad](https://www.datalad.org/) is
required. It is a free and open source command line tool, available
for all major operating systems, and builds up on Git and
[git-annex](https://git-annex.branchable.com/) to allow sharing,
synchronizing, and version controlling collections of large files. You
can find information on how to install DataLad at
[handbook.datalad.org/en/latest/intro/installation.html](http://handbook.datalad.org/en/latest/intro/installation.html).

## How to obtain (sub)datasets

A DataLad dataset can be `cloned` by running

```
datalad clone <url>
```

Once a dataset is cloned, it is a light-weight directory on your local
machine.  At this point, it contains only small metadata and
information on the identity of the files in the dataset, but not
actual *content* of the (sometimes large) data files.

DataLad datasets can contain other datasets, so called *subdatasets*.
If you clone the top-level dataset, subdatasets do not yet contain
metadata and information on the identity of files, but appear to be
empty directories.

The SFB 1451 superdataset contains one subdataset per project, and
these can have further subdatasets. In order to retrieve file
availability metadata in subdatasets, run

```
datalad get -n <path/to/subdataset>
```

After cloning a (sub)dataset, you can retrieve file contents, if they
are stored in a location available to you, by running:

```
datalad get <path/to/directory/or/file>
```
