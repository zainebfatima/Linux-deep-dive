Lab 50: Network File Transfers (wget/curl)

🎯 Objectives

- Understand and use "wget" and "curl" for network file transfers.
- Download files and webpages from URLs.
- Save downloaded content using custom filenames.
- Understand how to resume interrupted downloads.

---

🌐 What are "wget" and "curl"?

"wget" and "curl" are Linux command-line tools used to communicate with servers and transfer data over a network.

"wget"

"wget" is mainly used for downloading files and webpages.

"curl"

"curl" is a versatile tool used to transfer data to and from servers. It can display server responses directly in the terminal, download files, and perform many types of network requests.

---

1️⃣ Checking wget

wget --version

This confirms that "wget" is installed and shows its version.

---

2️⃣ Downloading a Webpage with wget

wget https://example.com

This downloads the webpage and saves it as a file, such as:

index.html

To view the downloaded HTML:

cat index.html

The terminal displays the HTML source instead of the graphical webpage shown by a browser.

---

3️⃣ Choosing a Filename with wget

wget -O webpage.html https://example.com

"-O" allows us to specify the filename for the downloaded content.

Check the file:

ls

---

4️⃣ Removing the Downloaded File

rm webpage.html

"rm" removes the file from the current directory.

---

5️⃣ Checking curl

curl --version

This confirms that "curl" is installed.

---

6️⃣ Fetching a Webpage with curl

curl https://example.com

Unlike "wget", "curl" normally displays the server's response directly in the terminal instead of automatically saving it as a file.

---

7️⃣ Saving curl Output to a File

curl -o web.html https://example.com

Here:

- "-o" = output to a file
- "web.html" = chosen filename

Important difference

curl -o filename URL

The user chooses the filename.

curl -O URL

"curl" uses the remote filename.

---

8️⃣ Resuming an Interrupted wget Download

wget -c URL

The "-c" option tells "wget" to continue an incomplete download when possible.

This is useful if a large download is interrupted because of a network failure or system shutdown.

---

9️⃣ Resuming with curl

curl -C - -o filename URL

"-C -" tells "curl" to continue from the existing downloaded portion when the server supports range requests.

---

🧠 Key Difference: wget vs curl

Tool| Main Use
"wget"| Mainly downloading files/webpages
"curl"| Transferring data and communicating with servers
"wget -O"| Choose output filename
"curl -o"| Choose output filename
"wget -c"| Resume an incomplete download
"curl -C -"| Resume an incomplete download

---

🔐 Cybersecurity Connection

Network transfer tools are useful in cybersecurity because security professionals frequently interact with web servers and remote resources through the command line.

They can be used for tasks such as:

- Retrieving webpages and files
- Inspecting server responses
- Testing web endpoints
- Working with APIs
- Downloading legitimate tools and resources during authorized security testing

---

✅ Lab Summary

In this lab, I learned how to:

- Use "wget" to download webpages.
- Use "curl" to retrieve server responses.
- Save downloads with custom filenames.
- Remove downloaded files using "rm".
- Understand the difference between "curl -o" and "curl -O".
- Resume interrupted downloads using "wget -c" and "curl -C -".

Lab 50 — Completed
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/946b6eb6-85e3-4168-bd1d-eb16801b7ce9" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/644e5123-f68d-436b-973e-69e99d3b566d" />

