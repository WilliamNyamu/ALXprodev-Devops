#/usr/bin/bash

# Automate the process of making API requests to the Pokémon API and saving the results to a file
# Calling the Pokemon API
HTTP_CODE=$(curl -s -o data.json -w "%{http_code}" "https://pokeapi.co/api/v2/pokemon/weedle/")
EXIT_CODE=$?
if [ ${EXIT_CODE} -eq 0 ]; then
    if [ ${HTTP_CODE} -eq 200 ]; then
        echo "API request successful. Data saved to data.json"
    else
        echo "API request failed with HTTP code: ${HTTP_CODE}"
    fi
else
    echo ${EXIT_CODE} > errors.txt
    echo "cURL command failed with exit code: ${EXIT_CODE}"

fi

