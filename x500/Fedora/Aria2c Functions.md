aria2c is the CLI for aria2, a downloader supporting HTTP/FTP/BitTorrent/Metalink.

Basic download:
aria2c <url>

Multiple URLs:
aria2c <url1> <url2> <url3>

Save to a different name/location:
aria2c --dir=/path/to/folder -o filename.ext <url>

Resume/interrupt:
aria2c -c <url>          # continue/resume partial download
# Ctrl+C pauses; re-run with -c to resume

Speed limits:
aria2c --max-download-limit=100K <url>
aria2c --max-upload-limit=50K  <torrent>

Segmented downloads (faster):
aria2c -x 16 -s 16 <url>   # 16 connections per server, 16 splits
aria2c -x 16 -s 16 -k 1M <url>  # also control min piece size

BitTorrent:
aria2c <file.torrent>
aria2c --seed-time=120 <torrent>      # seed 120 min, then exit
aria2c --seed-ratio=1.0 <torrent>     # seed to 1.0 ratio, then exit
aria2c -T <file.torrent> <url>        # download via HTTP+torrent together
aria2c --bt-daemon=true <torrent>     # seed-only mode (no files)

Magnet:
aria2c "magnet:?xt=urn:btih:<hash>..."

Metalink:
aria2c --metalink-file=file.meta4

Input file (list of URLs):
aria2c -i urls.txt
# alternative URLs for one file -> separate lines with tab between URLs

Auth / headers:
aria2c --http-user=user --http-passwd=pass <url>
aria2c --header="Cookie: token=abc" <url>
aria2c --ftp-user=user --ftp-passwd=pass <url>

Check / verify:
aria2c --check-integrity=true <metalink/torrent>

Help / version:
aria2c --help
aria2c -h                       # short version
aria2c --help=all               # verbose
aria2c --version

Notable common flags: -d/--dir (save dir), -o (output), -x (max connections), -s (split), -c (continue), -i (input file), -T (torrent file), -j (max concurrent downloads), -U/--user-agent.

To see everything organized by category: aria2c --help=all | less.
