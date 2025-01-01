# Property Owner Accountability

Mapping properties on the Montgomery County Rental Registry

=======
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

## Docker & Datasette

The Dockerfile in this repo wraps up both the scraping and the datasette server. To build and run a container:

```console
$ docker build -t rental_registry .
$ docker run -it --rm -p 8000:8000 rental_registry
```

After running, you can access the datasette server running on your local computer at http://localhost:8000

## Whiteboard Notes

Complainer
- Form
- Confirm corrections

Government Compliance
- Audit
- Data Entry

Owner Public Compliance
- Updating Regularly
- Sale / Change of owner
- Change of agent

Lookup 
- Public Safety
- Public Info
- Education

Brainstorming tasks
1. Compile Data - Rental Reg + Property ???
2. Geocode Data - Geocoder from Lotlinker
3. Mapit - Throw it into MontyLots
4. Other layers - As needed/desired
5. Repartioning - 311 Style

Additional Brainstorming
1. Existing registry list
2. Property DB
3. Compare & Find Noo
4. Non compliance list
