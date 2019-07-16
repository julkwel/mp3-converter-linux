# mp3-converter-linux
Convert mkv to mp3

`$ find . -type f -name "*.mkv" -exec bash -c 'FILE="$1"; ffmpeg -i "${FILE}" -vn -c:a libmp3lame -y "${FILE%.mkv}.mp3";' _ '{}' \;`

Convert webm to mp3

`
$ find . -type f -iname "*.webm" -exec bash -c 'FILE="$1"; ffmpeg -i "${FILE}" -vn -ab 128k -ar 44100 -y "${FILE%.webm}.mp3";' _ '{}' \;
`

Command to use it

`curl -s -L https://raw.githubusercontent.com/julkwel/mp3-converter-linux/master/converter.sh | bash`
