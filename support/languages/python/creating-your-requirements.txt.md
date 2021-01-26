# Creating your requirements.txt

## How it works: <a id="how-it-works"></a>

According to [documentation pip](https://pip.pypa.io/en/stable/user_guide/#requirements-files):

> “Requirements files” are files containing a list of items to be installed using pip install

That is, this file is nothing more than a text file, containing a list of **items/packages** to be installed during the **pip install** during the deployment process at Discloud.

### Let's take an example: <a id="example"></a>

 Considering this `requirements.txt` here:

```text
discord.pyseaborn==0.8.1pandas>=0.18.1
```

1.  **-e git+https://github.com/jtemporal/caipyra.git@master\#egg=caipyra**: That way we were able to install Python packages that are available on GitHub but not on PyPI. This is a really cool tip when, for example, you need the development version of a library or when you prefer to use a fork instead of the traditional version of the package.
2. **discord.py**: When we don't specify a version, **pip** will always try to install the latest version of the specified package.
3. **seaborn==0.8.1**: In the case of seaborn, we are installing version `0.8.1`. Fixing the version in this way is interesting because it ensures that your project will always be working since changes in the packages are indicated by the change in the version number.
4.  **pandas&gt;=0.18.1**: In the same way that the `==` sign defines a specific version to be installed, when we use the `>=` sign in this list we are saying that we want to install any version of the library, in this case pandas, be it version `0.18.1` or a last. Interesting in this case is to note that you can define a range of versions, for example, pandas **`>= 0.15.0, <= 0.18.1`**.

## ✍ How do I create my requirements.txt? <a id="how-do-i-create-my-requirements"></a>

You can use the **notepad** itself to create your file**`requirements.txt`**

![Creating a new text document and renaming it to &quot;requirements&quot;](https://gblobscdn.gitbook.com/assets%2F-LmveSmUr3rXxq5cvnW5%2F-Lo37pedEcHScUREaiNT%2F-Lo38VUKQA6g1lawDZuX%2Fimage.png?alt=media&token=1e154379-88a8-45b0-9c44-12d9e9239332)

![Example of the file created with some dependencies already defined](https://gblobscdn.gitbook.com/assets%2F-LmveSmUr3rXxq5cvnW5%2F-Lo37pedEcHScUREaiNT%2F-Lo38ccqqArRdA8v0lY7%2Fimage.png?alt=media&token=28e6e8be-b2bc-4185-986e-c09c075a3e4a)

## ✍ Automatically generating the requirements.txt file <a id="automatically-generating-the-requirements-file"></a>

A simple way to create your own dependency file is to use the `pip freeze`command as follows:

```text
pip freeze > requirements.txt
```

The `pip freeze` command lists the **Python** packages installed in your environment in the terminal already in the format that **pip install** can understand, by associating it with the redirection operator `>` you can write the same list that appears in the terminal inside the text file.

![](https://gblobscdn.gitbook.com/assets%2F-LmveSmUr3rXxq5cvnW5%2F-LqNJ2UAwWkmlo9zRSd_%2F-LqNJ4Kl4FXgmGC47AdD%2FCapturar.PNG?alt=media&token=14e0645b-483a-4b18-85b3-4fdf1c8a0cd2)

{% hint style="success" %}
Mass right? Now just create dependency files for all projects 😜
{% endhint %}

