<p align="center">
<h1>Steps to deploy an angular application into Azure blob storage</h1></p>

- Create a **Storage Account** in Azure Portal
![Create](https://lh3.googleusercontent.com/d4l-Yps9YhLMX1ILuYwd1denbuhKPko0EPRXNs188jXctodBHiJve4isNDkxMoS-5-M3KK6KmR_ClJO-jmQ6i4NgD9lpz_YfmGFTqX-ie4sDepsSN5UeYP39m6Zu6D6RrIWt40-tBMTnih70AnnFRlvr3zVLx6rrL7ITxBb6X3VKiizBoojxfCC5suXkR8ZnKSKgw5zVqypMnuQPRWEOAMdmSuH927QteJdiilrrAUBDsyh2YRo2o3G3oA79bYuHgfaf_bO6lMSVDuO_BT7LCoAnk432ESPP3QCw399jj2nu6kdHeRvSkKpRHB1_1KGupA6DBUyfq2yrTfKHqwUMlP5T6TknLPj7OgvHaGtKQosI-qxH8kBVe8X7XGkE3gxWso0sLguURGFv68QjzXU--bh_LWfU3OtYGJ65ewMSIOzJB52bca-hySyxNphBumkWFtCMF7fXdEvZsdtKoGC9Y5TQWSNb767C77hTCNsV8DA6nOGvYIgCMXA_FUzr1f3NlFfXbKmnRX73J7jSBXWmXv95QNb87PMFRSAaeJ_GXMNCp0WNH4P-CvAwM2govaK-y_1yioNP-qdslmXcozzGBeGv8b-g-iHWPFgSEEvEvYd4OHUsz771OEEhepD2RENPZBIn6y-FTlzIcq2E6khu_7OxAsEHfB31HPRtPfA27xpRYBogPO2ucxOLVIJFJSoKoTIaUMnIruFzrfdt4WB8og=w1006-h566-no?authuser=0)

- Click **Go to Resources** and navigate to **Static website** in the **Data management** section in the left side pane

- Turn the **Static website** switch to **Enabled**
- Enter the **index document name** as `index.html` and **Error document path** as `404.html` and **Save** the changes
![Static](https://lh3.googleusercontent.com/RJKhRrQVeR9-Sko82-0gEdNfFIxD2dNxViHLqIN5Ci9KZ4kJkFUSvM7GzHnS7yW0CVzs262yTRRRTqp_k6sB0OEMrducXweP4bRS3ISbU0r6-xgwPFpjLl2GL22eU4hCMsLF9uvyrzcAFZv5ar25bdBEeKH_9JRTarMmg4KkdyDh_IZPGPvqUodcQe5CgDVMozXzJheJTMgK1qWPBbGFQlokKvM9GVvWxpkhLJFf6Wf_P3XuVzi3AXC_JSsS2yWV20WoGAL9kjCdHotmngPKCQPQNhJY1ageFDMVUDt2uhfgA1Mw3c7uHHbMXxop607NYc2n9-26vp9YDelhmGIOcPiUcW7MHuks1FAY9byo5Xx_fU6SSS9DkgNkLRrqAGNUP-En-W74dHIsKwlLfpmPax3o3g4L1r37TNLvJpfkskVZ8_TM85Q-gG0Rao_f9-SJkJDqUMkIzzK4cgvzFjXowZZ3iz4kshpPog_fYQ-uS2oFuOprJXnoFdiUQAXgl8OsKxGPyczPBjEidd69fKdQyeXn5bbr0fGpzoEb59UyBBFNyiucxEkXd6L4yV4HPF5ZKvvHgTrsIN_pDkm5Nw0FHvb5_vMpi94iqhFuDBUuYnWYERe_x2EgYCGxs9alhA31ECJtGt_ZQzinpLXiit-YE-AHxPojvRJaUvi4v1TayZRMlqYXSe9zHZ3lNogXDpeWD8sc7nnTw6cwoYVupHd4uQ=w1006-h566-no?authuser=0)
- Open the terminal(Ctrl+Alt+T) and create an angular application using the following command 
`ng new {name of the application}`
``` 
ng new app
```
* Check if the application folder `app` contains the `dist`folder 
* If no use the command `ng build --configuration` / `ng build --production`
```
ng build --configuration
```
* After making sure that the `dist` folder is created, open the **VScode** and  install the extension **Azure Storage Account** from extensions.
* Now open the application folder in **VScode**(File->Open folder)
* Right-click on the `dist` folder and select **Deploy to Static Website via Azure Storage**
![Dist](https://lh3.googleusercontent.com/L8sd_cTA4kxnGkv1LI4Z9A48_LapJBdPz0cxNTI6W1Uzr0p8tUFjdCpVd_CqE0N6Qiu1iaoXiSkYbGL0TWA7DAnuoAwNWiSqnodW6gqyT5JwB22JwMVXFJ3VN0SO5i2hDgiBSSvnTqX9ZOY6k1VWpgEZ50R1W3FfN5G_D9s7tEWxAf6lno_F0TJYMHy3u2Q9lQ3msVTz2zanqDmZV-sRjdzFqCfDztyLFAl4Jyj09E5h65zWzdnFes3LSvDB1sgBUnhxnE8TFpO35Ca00ALbQNQGiZxLxiuUwIVxWN91k-cAE8ody4Up45S3xAPJ2s368o_vd4iOM7vNeuzjuayhjFFenGBvw6fFMeiFVBHerY0pGHAvvaXsEaf16yJ-aYAsvEyWwJ-CGEudHdF6CsvHudynrpM_I7Dc6joqiHvMbp5_djl_X9CRTnWELtUD1H3LNi7K747bDXRI09yzuTfYv6lDID1b2q692JMcW6IEMO6ewgYYt0WiUhbzRzv7ws9BPmsn6l_5onpqTWL3sP2ddlat0yAFWxKF_Hbl1pxsxKUIgp1MoZ1YflL5h7g_sLeY8e-3h6M-wjG-VwLgOCzTuQ5XghKj2NcyMcuOtrtqxLRYLv8qxpwOo6ZgL65l8QyA1NvaxCjrDSn5ZET8USk37WZy7SpirEeq-jbBDkUSfqBv1E8HboFttMu1_0JTy_wT474uAAJydbmvLnfmdUROvw=w1006-h566-no?authuser=0)
* Select the **Storage Account** from the appropriate **Subscription**.
* And application files will be deployed to the storage account selected.
![Deployment](https://lh3.googleusercontent.com/hcgqsqWWZwJRWYKXcfw3aT_0Ho7iw_slmDFP7mArb4RM0f_gEW9bx9B8LTjorle3IIJQ6b7-qqZmW_VlrWRTMgawNM2ciz8RuHNLUZNWb1ay_MTAW5wK72I_J57p0s1SmOGQ0_ul6Rqmxx7aK7BQZ0PMW-f29jFsHiMPAQLO0QnFgFFsYK5R2lxIiEunEYLXEH3f4dE5zB3IgtrW5_19h6E5sCkr4onD8aFFvWMZ-7UnvTIPgJxVrfcRk-HkiiDLfsQ3FKXNp-qFiOX1PwwCsm8K3oCuymPdDIOlIanbsuMPleWUjkoEswoslz2j-zPmaPf5Qj7DghCamS4oGk9RRcIRzWvWmRsAd-QZcvr6bJQDNqF491rv9JQdlrscqmUspQEuQRgijN5EHTI0UUcwfztrsMGd8hSd9Z0cz_e5TTCYyoXPHccR9W2AXIM43hNz4TCebAvo4wBmpjpHs6keh6Xrg02IINrUD-2Tfx-Zm1F6blBo-FUe7KhV73U7jkyLxFndp7mriwJyJhSYs5EWsNT-rjtQSb1hVhy-9N8iE38LugFsaWV_TqfX6ygQQsq0J3z2OEmu9F8NFjtEvJb5o8OjUUoTWbstnQOctFfRhItJ7XI_OlzpRZCEPG5lof54yYaWatZckek0GGMpqjDOAyk-wUDIy1RhRh2XL3rN3HqS3LBFGUjl7iCMzdOIJryPQjB-7BsVDtCcEOHMlE1efg=w1006-h566-no?authuser=0)
* Now open the **Containers** tab and click the **$web** to view the blob files.
![Container](https://lh3.googleusercontent.com/CO-hEO84cVm_V-VEEMk8gdt-8VSc-sN_KzdH5-eJjgRik719UserlcU3WlnwHn5mqP8eMz19dVgq8YhT1kEXq9_gZiIlFxYM50yVk1eF06aoTk_PAIWni1gKdga8TRuv0_ooQQ7xHMMWPQP9GarNjWorwaCwvjU5RVsvhsAKXYHGOQG-4J4SfUGiB5Qxw7CR5xxpAGNz0hxch2XTntJE2rG0ytwe6pZ2tisJSejnsgrnVdegtkszApy-ROOrv6AZZ46cCkLwtlj-VX9biajm36O-ZTAZVOOloSTbXLbTWhDNv1LxeeIt1Py9Hel7iOAhXEw-B8QH7PtW2xWQEIFmM62cW69-AK4-7zz9gbtCwJzqDIeDWv2og9U0oRkS0ASNEGFJGhQeW9KiGVqoac4_wqnH2u68699PQEZSl5PKE-qdr8CkO2UJi662V-h3Q60M3VDbkk_xFNTXDjM6J7K9LkBc5oTh3tNF8Mzj6erO2PEOJ6a_fgljppjScQZb8rWsW2EnGddOTscZm3UrnpFRPEne09iPfaqSMNrbrruVVZagMWas3fy71wD4H8dVYdQeK98t_iAzbdCEFGFclKoZAbhMeyw1BMaNy5d_lzBeyY_XOI1cJg_KFIHiqYBETBd2-Y3cnDvlvsXIO6IBFJeJDUD_Iec2shQUrBxHrYLFPp0LOcHb7K_GIdc-P8H7MYo3xS1PR304aZC4mXbxlzAALQ=w1006-h566-no?authuser=0)
- Now the list of application files can be seen uploaded as blobs.
![List of files](https://lh3.googleusercontent.com/JdSMMC6zR78rx5DfJm6ZrmMBMMVKK79UrIP5cGsW45mGordii0Fb8qqcOwVARkNR4Hqo9Gc6oG24SinouTkblBZNSmSGgTb-k7Y2pAaWA3yHFnWPSAfWUuvVXIGj2cLzWzFJXN0FSU3mYvnLycFiRq_3BWvk6y34F3qbDuDiV7OjGvv_3LFXHuVs0QO4AY5IhDhKizbOM7CC0tJitm8m4YkcP814f-63C_8vrmLSmrMh2hqNaUbi6wNW6_KFwovtYD49Vg_J4YIJjfH-Ei9A6yee4YGycDGbAuGn-cXm-IuF6qKCbfnb75C7zKZUwQm0l-Pm7pfLWcKaElBryai9jYb6zPUajWKlCdMc_wK26WYYmlJrQpeZV3JoZeZmf5h1c1OWfppq1KbYhVWAyH0b4TH9AuHId6xqLKMoVWF5Fr-yGdt_g3DdJGJU24T83tl1bhHeI-QN0zwQWQT5XzBUCcgmlJ-CtaWcHtf-3EmWDTE7wT0tLX6ZAD6HhtwR4uCC08DwctDwrT6f5rYneji1rc9qXpV3jcEKd-qAXMskbuMjzpm--tSzets9L5eyvRI5GNTRwZar8eTgkwvMxUng3zDaNkj9nis9pql_14h01RRE6unAuLF7ZlJG7-yXfgzkTDcX9kndudaKmvqus6NRm-KVC1hwOG6a5_Nz_FW2aT39C1ENN8h86tWx4JpcD1DVsXYZmB21SFaecaFleb755Q=w1006-h566-no?authuser=0)




