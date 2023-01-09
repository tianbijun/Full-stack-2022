Solutions of part 0 exercises to this folder

0.4: New note diagram

sequenceDiagram
Create a similar diagram depicting the situation where the user creates a new note on page https://studies.cs.helsinki.fi/exampleapp/notes when writing something into the text field and clicking the submit button.

code with Mermaid
```
sequenceDiagram
    browser->>+server: HTTP POST https://studies.cs.helsinki.fi/exampleapp/new_notes
    note over server:server asks the browser to do a new HTTP GET request to the address
    server-->>-browser: URL-redirect
    browser->>+server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.css
    server-->>-browser: main.css
    browser->>+server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.js
    server-->>-browser: main.js
    note over browser:browser starts executing js-code that requests JSON data from server 
    
    browser->>+server: HTTP POST https://studies.cs.helsinki.fi/exampleapp/data.json
    server-->>-browser: [{ content: "HTML is easy", date: "2019-05-23" }, ...]
    note over browser:browser executes the event handler that renders notes to display

```
[![](https://mermaid.ink/img/pako:eNqtU01P4zAQ_SsjX2lSFsRhc-C0CLTiS9vsCSM0xFPqktjBMwGqqv997To9oBUfB3Jx5Bm_9-bpzVo13pCqFNPTQK6hXxYfAnbaQfzug39hCsXx8V48nilUcFbX13B9NathIdJzNZ2yDMYSlw2XC2rZukdbzu2UXrHrW8K-nzp6uXNeiDNq-gUf0WAEzQcgPzLIgna0IB6MB4T4PvOentQQklCWVEy9aEwgHpEzUBH1FiNGBX__nBeBjA3UyMdTJfSvD9WhdbH8AfPbjm9kXX5GuvzP6V19Zy0LBmGgV2oGse4BllykJERPUXYeM_yeXV2CQUGYB9-NhJDBvzUiiSPK9u79yW7W0Hgn5KQCrc7qi3OwcQLklVaTJJLS_cH-j5_F_lFxcKgVbCZQluXtZ2ZkFyiHj54jAyzQmTZFMNvhDAXeIvA2lZb7FlfaqYnqKETPTVyhdeLRKoJ0pFUSY2iOQytaabeJrTiIn61coyoJA03U0CfV48apao4tx9uYVfHhIq_ldjs3_wBC20J-?type=png)](https://mermaid.live/edit#pako:eNqtU01P4zAQ_SsjX2lSFsRhc-C0CLTiS9vsCSM0xFPqktjBMwGqqv997To9oBUfB3Jx5Bm_9-bpzVo13pCqFNPTQK6hXxYfAnbaQfzug39hCsXx8V48nilUcFbX13B9NathIdJzNZ2yDMYSlw2XC2rZukdbzu2UXrHrW8K-nzp6uXNeiDNq-gUf0WAEzQcgPzLIgna0IB6MB4T4PvOentQQklCWVEy9aEwgHpEzUBH1FiNGBX__nBeBjA3UyMdTJfSvD9WhdbH8AfPbjm9kXX5GuvzP6V19Zy0LBmGgV2oGse4BllykJERPUXYeM_yeXV2CQUGYB9-NhJDBvzUiiSPK9u79yW7W0Hgn5KQCrc7qi3OwcQLklVaTJJLS_cH-j5_F_lFxcKgVbCZQluXtZ2ZkFyiHj54jAyzQmTZFMNvhDAXeIvA2lZb7FlfaqYnqKETPTVyhdeLRKoJ0pFUSY2iOQytaabeJrTiIn61coyoJA03U0CfV48apao4tx9uYVfHhIq_ldjs3_wBC20J-)
