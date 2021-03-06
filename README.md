<p align="center">
<h1>Steps to deploy an angular application into Azure blob storage</h1></p>

- Create a **Storage Account** in Azure Portal
![Create1](https://lh3.googleusercontent.com/eZMwednwDIdpYycx2NlDZ0UvGa5Q-gnZgjqBkSHcbCGmkIsUFpvpfC0QlEfYXl7igpFz3XBmoikqUH5HYTxThKDa6hDqJjlIzyO7YIhntIGduZKsBJeEgVhT9e-THF04LMQnKoyKa3K8PBNA2evvalm9Ukw_zFz8aHDGiSWga9V2QVqsAizwTg9y8CGpheu6CvC-j_PtW4Uu89kP7Gy3u57Ks6gQMy1pd-kW2005sJDwKMvaTBIu9mmygOUcwEaZsPgLA-83g5GQoHUYDgAdSZfxJd7Q0nrHtWG0idq4qGvBmf98IGbtacXHeToDwNrC2gyWDkl1GZr0yuDnQCu3okREAzfKzsBfPbxAK30oAm26i7vmr-NkLu4LyGa5OmRc9nRwrfQO-f_TyWUWX3euvrpLzJdQ46h8BM8YLaEnoUwyf_ItujLNTEyoCIDu7VzqaeUj6tRKH-xc1N_5W428ZHNqauDsxUfdXDsblgFUHTqXKKHU-rfXj6Tz5fwyBxtMV3Lc-4mIucSBLj7ZnzZSy4Rbp_qigAN1sRRR0dJlHITk-mmU8l5TvtPQ9feQkk2DOr9hlNTINc9rHiOU-Zhyf1BJR4gZlUIaIbktTa02LpaS9hsZNEZ9zRjbpsoxDPJUOhJj5Cb3CqpMtvHZKCSavJkqUDpARtkiZUu2HVxiJrSSvLr_qf1wnIeZ0wupiYoSoBh_WyLMCHRaL4KJymg5-7U=w1189-h668-no?authuser=0)

- Click **Go to Resources** and navigate to **Static website** in the **Data management** section in the left side pane

- Turn the **Static website** switch to **Enabled**
- Enter the **index document name** as `index.html` and **Error document path** as `404.html` and **Save** the changes
![Static](https://lh3.googleusercontent.com/Wm2PyVZavkczL9oC9LBQ0Kjj2mOpplReYrPCFAoKjXD33sN1iNkDn26dOg-nSOA7TCcmuhNdQFUPrLEo0kSfhTv-iZ7cfksBWf3dmNswqVgkMnvDXp0JVdLkeU-G6lxIV5Qf62sSetmJ-61fQZjo727OC9D4ibfefsvNhofVFV9irLEJwjxVjtb-2cjvleQSDt7a-yCQmLRzNuCSjoFgg1uem6Y7m36g8_Ae4Tn3y0-XiQcST7fiwr1JTyvc4ufRmbRK6-fubWSuiURqoDatiUkVXv_8S6qE0Gy59shy8sMjlG-pR2uMFwIBMKHqytopu4ck3syaMm6f6Rfsmpa5hHeq2kOuBGIhTxbhxS7cGvyzYWDQH3zWLb_6B29i3DwY0n8lBrUC2reW31l_CennkkFgyDoBY7jYR2me9Mr9t0AkYsD7PttEv_D1wRAb9O1zXtDelTpNsBvFLu7o2Wsgllljfm8nadoMZl3HJr5erZRDzLMx2xKRT04IXvBcy-KMHHGH6InsDDSIKLZ696klKgWppVyojT7mhKoZzsuG-g_hD_XILQGTZ3rlGaE21s0X-NuAG1BP8H1YyW4kXdlg5oh1pgi0ITyU55sex8IrbZcBdZKc9BCtCyNq2zxoWVjIhsX4zco_T8XI3mWKdaEXBwTPo_nZvuGCOEUmVJnUEjXxsM0a2jO35eouACP8zPX8RA9GqYMI7AEibb5Aua7c1us=w1189-h668-no?authuser=0)
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
![Dist](https://lh3.googleusercontent.com/14JGRYVB1JUZgiirX9jFJpBc-FEb3TC-cj8tP3gV4evscaWyMOPo-_eFHVrRTTvpRz8vTHDo3dh9y7c6b-FdaYx7B9ENBsiC2u1GZMlaoyH85loHwmsC3hmq0S7mbT5klVsrvU01euD_1qiLA3Vt23NJSSxxgTP2wCKpJJT0mdrLQbOLVRUtizkin4welrGacpmDGkbkWr8C9Q8g3DM7wYPDbrs3sphJ3VITM-0vFw5lyDafSKhTYu0vcBV1Z5RuDt_3oCMmAqMXw-_AP4SKuzhTQZ7DHIu5A7PgHvm2MXgnkjUPIkSBVxyK8s8hXrtx2TLyIruEMPPnata3RVkd9eJ1ngxo36QLB2bMNbIQWo-I31X88wJdLNBTwDIJfyUlmd1Gz5CdszjlTh63zZ-owEU6nwQ_9Oaf3xYxr6ll6FNxmTyJpNY3z1jgKFlN3oO7DyAi9hvNa-577IGFIDoG0t1nF7spq0KUVFgDT6-46WpjP-MQ_CjEe6Vdb1Ncb1EAOmMDqfiDkQToH0q5g33T2k0ME3XFxYZSA_vmry8yhz7JGQgARXHpAVf9BzEUVGxavUQYh3ueYPg2z4plBYeQhnFn0dqhaZFAQ0tC_EJeYST0txTKn-BNQEgu2uLjFe108EzB5gL_W8YFdha0QrmaXnYo9Iqblx1-joggM9IcyyJhdRId8ZeTknzERMCsTFVhtsrmGkxwe5CaglF3tVbp9HA=w1189-h668-no?authuser=0)
* Select the **Storage Account** from the appropriate **Subscription**.
* And application files will be deployed to the storage account selected.
![Deployment](https://lh3.googleusercontent.com/z2d9t2bOzi_P-aO66sEB0qPJNjzw3iI-SA710WbYIcggtICPX2cmiKadusMKPAPgXSn6L2ByFo7V-bB0T1DeVOYcZpV_VuO4NVQBFyHH3gUyT_1J-n8NlcIHSkF4GCXqafYMAAk1ft12UhmA4LqL7PEZOYOaqfnZgpIxk3s_3wJOY8NhV5AEfz5IRjWXuEcvSlXapIL77ewsUm-1l-A2EhUTLOA6hkQEWCUkxm5IWSttN9OkqbEXpyej_Tmn56mbJ7g4W4FqQ87rgJaUs-rrebLtyooge3AQymgdvFuEA2eY1gkm2EpXrQkvxnR1LYNR-5Spk5DEOrKJU2G1L7hWVxUUC525OCAkjga2f6Uy_WBKcZR4s-6Zc4_s24Gi1PWXUsK8YjU2fMJt9JjqetP_ZfxzFzeAi0-6OkOdsLnZWEhIlcEC37BxtJxAp-Yga_9AgToNFb9BQUmpZFUPqT5DqciWPxv7MqR-cjXT-W4iXbthrOkIRH0t-xTYSPhbDeNL_yBfmLxo6eJdJ9_gU0FBAgoMz-kA2rWgbBFCvotJz90_DLSepmvmIMzRmbwwFj8o3Gxwye4BxIk82Zf1zlDGhxAGXP8zo7ntLeRdc88sGrc-G8hpqgxewLoLbkAmiLqXZC_f0TIIXSXoBixEIIqSUt_VVm2CBWqk9U64_jwb26kp5XZfNQuhB5kDPQrEkq9PaxWM4Kvth3b14RT9uKJvQFQ=w1189-h668-no?authuser=0)
* Now open the **Containers** tab and click the **$web** to view the blob files.
![Container](https://lh3.googleusercontent.com/-K8My5YbhlgEOGKdWyA6V4NuH4bkUhFtDtSUIVQXpTeVDbPFYq22gVHhcAHnQE7pBgG4rkFRsLkHP5vbIS6OkM51s8pH7G-FjN8WTS5cTqcRSpmo4I8KBzjoquw6lP7kKA-kHEnEqReU1xFhb_vVexEPxjkPf7cOCgrhSU-0uk3rOE4eE14H60CkKIQhSIg7B85QDZpEQpFCmlbVDa4Mq0TLTIknt6asZqnlETRBT6cDRwFsE2GkniwS3YhcTQUJNfZ-vP9mwpXrm4VDoa817-o4bI5YawJs1Dnw3RuWF9BYk6U3mpI-KDS53Qt-0dft3O2oLgvJWbRcPk1DYOtenFhDCj7gpD-x2HOUB5ouf53J0yoOYf9GhRCPDicu1nJH9S9t6XFNEwiPXamNkr0RY6U4XFeDIcVh4YLBg0A5KJ_Go_lsBwY_NHCA9qdINV9v29CbG3uI4FHFULSNsq6V8uoR4kwMabm37W8MvJpN9VpvbV9QGdA1VVq2yihLSQSYioqlqQykUxdBGoI6BeuOr4ehPsXDMKVTeWMb1JdsGdzkzO4yu67NMMqVmV7gV1r4zGWW2_fsWFSv8BOxNw-E3UCT8FlNtQPUj0QoJD0Co62ysyMI_h2d6bHF6BA9GJ26ffLgIXEmU5Fd1xGeUXPTnYf2gOwQA4t6IQRl2wt-R0SHpcjQTMBWLgj1NXGHOgn6Fnqx8r_mjyOYEU-GU0bcenQ=w1189-h668-no?authuser=0)
- Now the list of application files can be seen uploaded as blobs.
![List of files](https://lh3.googleusercontent.com/Hahiyz-jLpFZkjJlppYenWZWzKBo3jldZYtsPVViJrVp6URs2g2viTRb8X-ohB0P79P3LxxLSw0UlKavxTopaCKTxQIOI-8CEUc8l0SXcGNsaTqyVRXmSjfthqNLXizUa2JFj-JtSExW-F6pnKkYhQry3nSRFRDNr44DWp_kexMwO4hf1AKzWhGC9OhgBGR6yNMFL_T0CeEgEPQKrEGCNY4T8V7jeDZvrJ_LDNNb-UKgiNTL7JG71NKdU-53WYk83VjdH03jzWs2tgog2IC0kXV2qyv6pWWuhlyO3CXP3Ej46BGYzvivu3gy_-Ton9e144JR7b5i026O4oXhC4mtWyPZ_oYhGMNSQijdRQsZ7RrJRmLB0eHuTLAYXB-kIMjpnAvQvAvI3g39tzR82pSS545s11VtkL8IT-vhtNwb5vqWNWz7IF6qe2MJ_siQSWvJwFMcTVVdSg6S0qYmxMx1Nhd0aORULvMQr8Ty5M87YC0tOcWqG0MI-LQM5b8uTsa-p4Er0lhnF2LzoTBIhddJyQL0dNEHi28ufkuWsdFLg2MW8wbVk9c6B2kSEGZwc0wcRgG4hjo-Csk40PTiuhhlROfg128V9TM2mIiTC3Q5InbTmTdqyLcScCYeNApybwu2lO6pFkBvHteelLBsKkJ0X5FCZ72aSG7HTl5cmNXkJcBpV2dUXWxgWPDyk_G5cxsAc1com79t353ZPTgxIeirpbw=w1189-h668-no?authuser=0)
* Now enter the primary endpoint from the **Static Website** blade to view the output
![Output](https://lh3.googleusercontent.com/_VpjDlqQ7Nt1pmpZL3TrB5NgY6-vchJar1G8Xfxam0gG9tzh8qYY0L_DP28vUBtbmtf3BLxf27txLOdEsuOQkjx0BYrTIVd_TE9ut7jHJFrAlZtffZVZhfIAUghhh-s6INyt2IJ1SeOc-U-pRwAFiKMj0GenbWn2RHCAKfkTamJTl8QPBwItkcKMqz9eLdAJLJdoWoVjjldZU6DZhNCXWOatc7--V9NvwdbEzgicFCzA8RBQyUNDUVom1E98Pdpm2a-X-WoJwyObVd2FmOcgGcgWN92eb98zAzb40m1VNknmHFZbzgwH6CJ0MPmCTL5ppf9fCp34kuNWklPYlp-L92qjtUqsDxIQ7AIuEwOntc4QIs5Kgah_Xqv1dk5RnIrRUnGb8lxc53AM-TOUnPqI3bLGwk6NHHba_YlAGsXKHaySt-gRHCc7i70P_kpwhjCktwrmW1N2NyEtU7emW0gTixJT0pa3VBbiv_Aj0P7AcnObNrB9IjHOGwKKh3Mgy6sWtgQSxx5bYYoO3LOVbr7lFqv0Bp4FpVoFg9p9h_9RhSf53vYv3rkYn8n272-bu1RaWPAq_dvFrc-LMYPMJ0skoFjgpal_cGCa4dftYrxoSjSjlg8L8_AXgEk-77kcNR4gQGb6GJKGle2OfUYIDOa68cl-MsPkLiGC2RLS0Oa551GLmju2fibg3K9t5X6ewHgQ8WDjDRW9QDAAOfIMqLopvRw=w1189-h668-no?authuser=0)




