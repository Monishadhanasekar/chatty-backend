### User Login flow
```mermaid
sequenceDiagram
    actor u as user
    participant f as Frontend
    participant ws as Web server (backend)
    participant mdb as mongoDB
    autonumber
    u ->> f: Enter username, passowrd and click Login
    f ->> ws: /api/auth/login
    ws ->> mdb: Get user details
    alt passowrd incorrect or user not found
    ws ->> f: return http status 400
    f ->> u: Show error
    else password correct
    ws ->> f: send user details
    Note over f: load chat applicaiton
    end 
```

### WebSocket connection flow
[![](https://mermaid.ink/img/pako:eNplkUFPAyEQhf_KhJMmbXrn0ERT_QMevGxiZmHYEmGmAqtpmv53B3f1YPfE8r735gEX48STsabSx0zs6BBxKpgHBv3QNSmAgBXmSgUelu0TlhZdPCE3CF18LsKN2N_KX7XrrzSC-j814m5E967o_S2b_djhLDzJ4XHRWRqBdGOwSwdMhdCfIck0kY-8cK5EzcEET7XhmGI9au0qOqqBE2ZyLcrKBthu93utZgG93_bU_8O6VvXs9DPzLfrNGqZLiAyZspTz4vo7t-ausTuc23GHKXV33V3WkOvC6Z10UI9rYdJ-ykE7EoQSNatC0Dvv_91lNiZTyRi9vtGl-wejWqbBWF16CjinNpiBr4rOJ4-NnnzU6sYGTJU2RrvIy5mdsa3M9Aut77xS129j-bC2)](https://mermaid.live/edit#pako:eNplkUFPAyEQhf_KhJMmbXrn0ERT_QMevGxiZmHYEmGmAqtpmv53B3f1YPfE8r735gEX48STsabSx0zs6BBxKpgHBv3QNSmAgBXmSgUelu0TlhZdPCE3CF18LsKN2N_KX7XrrzSC-j814m5E967o_S2b_djhLDzJ4XHRWRqBdGOwSwdMhdCfIck0kY-8cK5EzcEET7XhmGI9au0qOqqBE2ZyLcrKBthu93utZgG93_bU_8O6VvXs9DPzLfrNGqZLiAyZspTz4vo7t-ausTuc23GHKXV33V3WkOvC6Z10UI9rYdJ-ykE7EoQSNatC0Dvv_91lNiZTyRi9vtGl-wejWqbBWF16CjinNpiBr4rOJ4-NnnzU6sYGTJU2RrvIy5mdsa3M9Aut77xS129j-bC2)

### Chat flow
[![](https://mermaid.ink/img/pako:eNq1lE1v2zAMhv8Kp1MKxOjdGAK0SIfde9jFQEtJdCJUH54ktwiC_PdRVpw46HbalpMiviSfl7R9FCpoEq1I9HMkr2hrcBfRdR74hyqHCAiY4MEaRfV2wJiNMgP6DP0U_BaDz-Q1PHxWfKSi-EESEsV3irCSqN5YfPebavKm2uOSYgo9Bvk5y-kp5oLfhe2cA81mw3Qt2IAa1B5zPgAOQw2raDgdLTyljNKatOeMFJgrgwrek8om-Kpli00p9pFaQK2bkX3UiA-ZIBRPJZaYkqBEX4xen6vxEYwHRy7EQ81iZ_UgK6P8F4zyPzFe5_jMd7xKlqWEO4LX76as48vrZSGT5BLP4bqt5QgTixqXdqscXi4g_P-uUn6VcUOzYdJ_MnxrqzeFLe9p4ajnZ6bclB4gg5wqAzJhunVSC_Jj2szrYJomkjL0Tqs-BvcXnH1dMhfdmjRYPExMN51xnnVfh10M3Z8V97xM7lnZj4VlzYOdOE5Xbk7id2De7qJBXet0TIxm7RKNpyDWwlF0aDR_AY7luhOc7qgTLR819Tja3InOn1g6DhozPWnDbUTbo020Fjjm8HzwSrQ5jjSLzl-Rs-r0CzmqeJY)](https://mermaid.live/edit#pako:eNq1lE1v2zAMhv8Kp1MKxOjdGAK0SIfde9jFQEtJdCJUH54ktwiC_PdRVpw46HbalpMiviSfl7R9FCpoEq1I9HMkr2hrcBfRdR74hyqHCAiY4MEaRfV2wJiNMgP6DP0U_BaDz-Q1PHxWfKSi-EESEsV3irCSqN5YfPebavKm2uOSYgo9Bvk5y-kp5oLfhe2cA81mw3Qt2IAa1B5zPgAOQw2raDgdLTyljNKatOeMFJgrgwrek8om-Kpli00p9pFaQK2bkX3UiA-ZIBRPJZaYkqBEX4xen6vxEYwHRy7EQ81iZ_UgK6P8F4zyPzFe5_jMd7xKlqWEO4LX76as48vrZSGT5BLP4bqt5QgTixqXdqscXi4g_P-uUn6VcUOzYdJ_MnxrqzeFLe9p4ajnZ6bclB4gg5wqAzJhunVSC_Jj2szrYJomkjL0Tqs-BvcXnH1dMhfdmjRYPExMN51xnnVfh10M3Z8V97xM7lnZj4VlzYOdOE5Xbk7id2De7qJBXet0TIxm7RKNpyDWwlF0aDR_AY7luhOc7qgTLR819Tja3InOn1g6DhozPWnDbUTbo020Fjjm8HzwSrQ5jjSLzl-Rs-r0CzmqeJY)
