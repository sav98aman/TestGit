```
OkHttpClient client = new OkHttpClient();
RequestBody body = new FormBody.Builder() 
			.add("token", "{TOKEN}")
			.add("to", "")
			.add("body", "")


            .build();

Request request = new Request.Builder()
  .url("https://api.ultramsg.com/{INSTANCE_ID}/messages/chat")
  .post(body)
  .addHeader("content-type", "application/x-www-form-urlencoded")
  .build();

Response response = client.newCall(request).execute();
 
 System.out.println(response.body().string());
```
