### [C#] Discord AutoReg Bots BAN

Simple function to check if user is AutoReg

First Hook an Event 
```cs
_client.UserJoined += functionname;
```

Then Create a function

```cs
private async Task functionname(SocketGuildUser user){
    if (user.CreatedAt <= DateTime.Now.AddHours(-12))
            {
                await user.BanAsync(0, "AutoBan");
            }
}
```

If you want to change Time difference just change **AddHours(-12)** to **AddDays(-1)** and it will ban every new joined person that account was created 1 day ago.
