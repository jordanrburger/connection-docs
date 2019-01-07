---
title: Dropbox
permalink: /writers/storage/dropbox/
---

* TOC
{:toc}

This extractor writes tables as CSV files or other files into a single [Dropbox](https://www.draopbox.com/) account.

## Create New Configuration
Find the Dropbox writer in the list of writers and create a new configuration. Name it.

{: .image-popup}
![Screenshot - Create configuration](/writers/storage/dropbox/ui1.png)

As the next step, click the **Authorize Account** button. Select one of the two authorization methods:

{: .image-popup}
![Screenshot - Authorize account](/writers/storage/dropbox/ui2.png)

- **Instant** – Use this if you have access to the Dropbox account; the authorization will be done immediately.
- **External** – If you need to authorize access to the service from someone who does not have an account in KBC, you can generate an external link, which will guide them through this process.

## Add input
You may specify Storage [tables](/storage/tables/) or [files](/storage/file-uploads/) to be written the the target Dropbox account. To specify tables, click the
**New Table Input** button and select a table you want to send to Dropbox. Filename is the name of the destination file, directory `/data/in/tables/` is ignored.
To specify files, click the **New File Input** and specify file tag or [Elastic Query string](https://www.elastic.co/guide/en/elasticsearch/reference/6.6/query-dsl-query-string-query.html#query-string-syntax).

{: .image-popup}
![Screenshot - Specify input](/writers/storage/dropbox/ui3.png)

The written files will be available in the **Apps/Keboola Connection Writer V2** folder in Dropbox. You can optionally specify additional subfolder
in this folder in the `Destination folder` setting. In the above screenshot, the files would be saved in the folder
`Apps/Keboola Connection Writer V2/samples/monthly`. The configuration can write as many tables and files as you wish.