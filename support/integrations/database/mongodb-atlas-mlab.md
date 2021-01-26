---
description: Setting up your Mongo Bank in a Bot hosted at Discloud.
---

# MongoDB Atlas \(mLab\)

![](https://gblobscdn.gitbook.com/assets%2F-LmveSmUr3rXxq5cvnW5%2F-LpzgENRhbRfczme6uGD%2F-Lpznrclqb05WJ9xtxJn%2Fmaxresdefault.jpg?alt=media&token=b0a3298a-c1fc-4701-b759-f2cfb6868d52)

## When connecting your bank [MongoDB](https://mlab.com/) to a Bot Discord hosted on DisCloud you may come across the possible error:

{% hint style="danger" %}
```javascript
Erro ao Conectar na MeuDB: MongoNetworkError: connection 0 to meudb-shard-00-00-9m7sg.mongodb.net:27017 closed
```
{% endhint %}

You will receive this error message if you have not included the MongoDB Atlas addresses, the IP where your Bot is hosted, on the white list.

{% hint style="info" %}
**Due to the way DisCloud works, we are unable to provide you with an IP address.**
{% endhint %}

So according to the [documentation ](https://docs.atlas.mongodb.com/security-whitelist/)MongoDB Atlas, the **only way to get DisCloud** instances to connect to your bank, is to add **0.0.0.0/0** \(that is, **all addresses**\) to your MongoDB Atlas **whitelist**.

![](https://gblobscdn.gitbook.com/assets%2F-LmveSmUr3rXxq5cvnW5%2F-LpzgENRhbRfczme6uGD%2F-LpzoGSi0gyQNq_6a99v%2FCapturar.PNG?alt=media&token=856efef3-07c2-4746-a878-62160fdf6626)

