# Stored XSS in Azure cloud shell

## Steps for reproduce:

1. Open https://portal.azure.com/ and go to Azure Cloud Shell:

![](1.png)

2. Create file using xss payload as name;

### We will need to call error message in future. I used limitation of rights;

3. Change permissions for file like this:

![](2.png)

4. Open created file using editor in portal:

![](3.png)

5. Click "Save" or "CTRL+S";

6. Alert.

![](4.png)
![](5.png)


## Timeline

- 24.11.2020 - Report was created on https://msrc.microsoft.com/
- 03.12.2020 - Reward ($1200)
- 11.01.2021 - Fix has been applied
