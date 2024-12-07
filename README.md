# Property Owner Accountability
Mapping properties on the Montgomery County Rental Registry

## Scrapy

This is a [Scrapy](https://docs.scrapy.org/en/latest/index.html) project.

## Usage

This project uses [Poetry](https://python-poetry.org/) for dependency management.

```console
$ poetry install
$ poetry shell
```

Run the spider and output to a sqlite3 database:

```console
$ scrapy crawl rental_registry -o output.db
$ # Open with datasette:
$ datasette output.db
```

Alternatively, you can output to a jsonl file for quicker reading:

```console
$ scrapy crawl rental_registry -o output.jsonl
```
