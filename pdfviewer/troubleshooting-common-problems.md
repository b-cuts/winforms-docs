---
title: Troubleshooting Common Problems
page_title: Troubleshooting Common Problems | UI for WinForms Documentation
description: Troubleshooting Common Problems
slug: winforms/pdfviewer/troubleshooting-common-problems
tags: troubleshooting
published: True
position: 15 
---

# Troubleshooting Common Problems

This article describes common problems that can be encountered when using __RadPdfViewer__ and their solutions.

## PDF retrieved from database is not shown correctly

There are several perquisites that have to be fulfilled in order for a PDF file to be loaded correctly. Some of them are listed here.

When retrieving a file as a byte array from database and creating a __MemoryStream__ from it, there are cases when the retrieved file is not shown correctly. This is usually due to additional NULL(0) bytes appended to the end of the document when it was stored in the database.

PDF files have to end with %%EOF marker, so this essentially makes the document invalid and __RadPdfViewer__ is unable to show it. __RadPdfViewer__ is looking for this marker in the last 1024 bytes and if it does not find it, throws an exception.

In order to fix the issue, you can manually trim the additional (null) bytes. 