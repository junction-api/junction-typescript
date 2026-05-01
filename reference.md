# Reference
## Link
<details><summary><code>client.link.<a href="/src/api/resources/link/client/Client.ts">listBulkOps</a>({ ...params }) -> Junction.BulkOpsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.link.listBulkOps({
    nextCursor: "next_cursor",
    pageSize: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.ListBulkOpsLinkRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LinkClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.link.<a href="/src/api/resources/link/client/Client.ts">bulkImport</a>({ ...params }) -> Junction.BulkImportConnectionsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.link.bulkImport({
    provider: "oura",
    connections: [{
            userId: "user_id",
            accessToken: "access_token",
            refreshToken: "refresh_token",
            providerId: "provider_id",
            expiresAt: 1
        }]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.BulkImportConnectionsBody` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LinkClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.link.<a href="/src/api/resources/link/client/Client.ts">bulkTriggerHistoricalPull</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.link.bulkTriggerHistoricalPull({
    userIds: ["user_ids"],
    provider: "oura"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.BulkTriggerHistoricalPullBody` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LinkClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.link.<a href="/src/api/resources/link/client/Client.ts">bulkExport</a>({ ...params }) -> Junction.BulkExportConnectionsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.link.bulkExport({
    provider: "oura"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.BulkExportConnectionsBody` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LinkClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.link.<a href="/src/api/resources/link/client/Client.ts">bulkPause</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.link.bulkPause({
    userIds: ["user_ids"],
    provider: "oura"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.BulkPauseConnectionsBody` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LinkClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.link.<a href="/src/api/resources/link/client/Client.ts">token</a>({ ...params }) -> Junction.LinkTokenExchangeResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Endpoint to generate a user link token, to be used throughout the vital
link process. The vital link token is a one time use token, that
expires after 10 minutes. If you would like vital-link widget to launch
with a specific provider, pass in a provider in the body. If you would
like to redirect to a custom url after successful or error connection,
pass in your own custom redirect_url parameter.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.link.token({
    userId: "user_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.LinkTokenExchange` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LinkClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.link.<a href="/src/api/resources/link/client/Client.ts">codeCreate</a>({ ...params }) -> Junction.VitalTokenCreatedResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Generate a token to invite a user of Vital mobile app to your team
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.link.codeCreate({
    userId: "user_id",
    expiresAt: new Date("2024-01-15T09:30:00.000Z")
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.CodeCreateLinkRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LinkClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.link.<a href="/src/api/resources/link/client/Client.ts">generateOauthLink</a>({ ...params }) -> Junction.Source</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint generates an OAuth link for oauth provider
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.link.generateOauthLink({
    oauthProvider: "oura"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GenerateOauthLinkLinkRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LinkClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.link.<a href="/src/api/resources/link/client/Client.ts">connectPasswordProvider</a>({ ...params }) -> Junction.ProviderLinkResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This connects auth providers that are password based.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.link.connectPasswordProvider({
    provider: "whoop",
    username: "username",
    password: "password"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.IndividualProviderData` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LinkClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.link.<a href="/src/api/resources/link/client/Client.ts">completePasswordProviderMfa</a>({ ...params }) -> Junction.ProviderLinkResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This connects auth providers that are password based.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.link.completePasswordProviderMfa({
    provider: "whoop",
    mfaCode: "mfa_code"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.CompletePasswordProviderMfaBody` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LinkClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.link.<a href="/src/api/resources/link/client/Client.ts">connectEmailAuthProvider</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This connects auth providers that are email based.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.link.connectEmailAuthProvider({
    provider: "freestyle_libre",
    email: "email"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.EmailProviderAuthLink` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LinkClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.link.<a href="/src/api/resources/link/client/Client.ts">getAllProviders</a>({ ...params }) -> Junction.SourceLink[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET List of all available providers given the generated link token.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.link.getAllProviders();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetAllProvidersLinkRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LinkClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.link.<a href="/src/api/resources/link/client/Client.ts">connectDemoProvider</a>({ ...params }) -> Junction.DemoConnectionStatus</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

POST Connect the given Vital user to a demo provider.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.link.connectDemoProvider({
    userId: "user_id",
    provider: "apple_health_kit"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.DemoConnectionCreationPayload` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LinkClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Electrocardiogram
<details><summary><code>client.electrocardiogram.<a href="/src/api/resources/electrocardiogram/client/Client.ts">get</a>({ ...params }) -> Junction.ClientFacingElectrocardiogramResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get electrocardiogram summary for user_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.electrocardiogram.get({
    userId: "user_id",
    startDate: "start_date",
    endDate: "end_date",
    provider: "provider"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetElectrocardiogramRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ElectrocardiogramClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## SleepCycle
<details><summary><code>client.sleepCycle.<a href="/src/api/resources/sleepCycle/client/Client.ts">get</a>({ ...params }) -> Junction.ClientSleepCycleResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get sleep cycle for user_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sleepCycle.get({
    userId: "user_id",
    startDate: "start_date",
    endDate: "end_date",
    provider: "provider"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetSleepCycleRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SleepCycleClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Profile
<details><summary><code>client.profile.<a href="/src/api/resources/profile/client/Client.ts">get</a>({ ...params }) -> Junction.ClientFacingProfile</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get profile for user_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.profile.get({
    userId: "user_id",
    provider: "provider"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetProfileRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProfileClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.profile.<a href="/src/api/resources/profile/client/Client.ts">getRaw</a>({ ...params }) -> Junction.RawProfile</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get raw profile for user_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.profile.getRaw({
    userId: "user_id",
    provider: "provider"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetRawProfileRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProfileClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Devices
<details><summary><code>client.devices.<a href="/src/api/resources/devices/client/Client.ts">getRaw</a>({ ...params }) -> Junction.RawDevicesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get Devices for user_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.devices.getRaw({
    userId: "user_id",
    provider: "provider"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetRawDevicesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DevicesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Activity
<details><summary><code>client.activity.<a href="/src/api/resources/activity/client/Client.ts">get</a>({ ...params }) -> Junction.ClientActivityResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get activity summary for user_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.activity.get({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetActivityRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ActivityClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.activity.<a href="/src/api/resources/activity/client/Client.ts">getRaw</a>({ ...params }) -> Junction.RawActivityResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get raw activity summary for user_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.activity.getRaw({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetRawActivityRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ActivityClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Workouts
<details><summary><code>client.workouts.<a href="/src/api/resources/workouts/client/Client.ts">get</a>({ ...params }) -> Junction.ClientWorkoutResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get workout summary for user_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.workouts.get({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetWorkoutsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WorkoutsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workouts.<a href="/src/api/resources/workouts/client/Client.ts">getRaw</a>({ ...params }) -> Junction.RawWorkoutResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get raw workout summary for user_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.workouts.getRaw({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetRawWorkoutsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WorkoutsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workouts.<a href="/src/api/resources/workouts/client/Client.ts">getByWorkoutId</a>({ ...params }) -> Junction.ClientFacingStream</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.workouts.getByWorkoutId({
    workoutId: "workout_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetByWorkoutIdWorkoutsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WorkoutsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Sleep
<details><summary><code>client.sleep.<a href="/src/api/resources/sleep/client/Client.ts">get</a>({ ...params }) -> Junction.ClientSleepResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get sleep summary for user_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sleep.get({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetSleepRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SleepClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.sleep.<a href="/src/api/resources/sleep/client/Client.ts">getRaw</a>({ ...params }) -> Junction.RawSleepResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get raw sleep summary for user_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sleep.getRaw({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetRawSleepRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SleepClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.sleep.<a href="/src/api/resources/sleep/client/Client.ts">getStreamBySleepId</a>({ ...params }) -> Junction.ClientFacingSleepStream</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get Sleep stream for a user_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sleep.getStreamBySleepId({
    sleepId: "sleep_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetStreamBySleepIdSleepRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SleepClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Body
<details><summary><code>client.body.<a href="/src/api/resources/body/client/Client.ts">get</a>({ ...params }) -> Junction.ClientBodyResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get Body summary for user_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.body.get({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetBodyRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BodyClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.body.<a href="/src/api/resources/body/client/Client.ts">getRaw</a>({ ...params }) -> Junction.RawBodyResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get raw Body summary for user_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.body.getRaw({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetRawBodyRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BodyClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Meal
<details><summary><code>client.meal.<a href="/src/api/resources/meal/client/Client.ts">get</a>({ ...params }) -> Junction.ClientFacingMealResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get user's meals
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.meal.get({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetMealRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MealClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## MenstrualCycle
<details><summary><code>client.menstrualCycle.<a href="/src/api/resources/menstrualCycle/client/Client.ts">get</a>({ ...params }) -> Junction.MenstrualCycleResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.menstrualCycle.get({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetMenstrualCycleRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MenstrualCycleClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Vitals
<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">workoutSwimmingStrokeGrouped</a>({ ...params }) -> Junction.GroupedWorkoutSwimmingStrokeResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.workoutSwimmingStrokeGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.WorkoutSwimmingStrokeGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">workoutDistanceGrouped</a>({ ...params }) -> Junction.GroupedWorkoutDistanceResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.workoutDistanceGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.WorkoutDistanceGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">heartRateRecoveryOneMinuteGrouped</a>({ ...params }) -> Junction.GroupedHeartRateRecoveryOneMinuteResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.heartRateRecoveryOneMinuteGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.HeartRateRecoveryOneMinuteGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">waistCircumferenceGrouped</a>({ ...params }) -> Junction.GroupedWaistCircumferenceResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.waistCircumferenceGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.WaistCircumferenceGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">leanBodyMassGrouped</a>({ ...params }) -> Junction.GroupedLeanBodyMassResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.leanBodyMassGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.LeanBodyMassGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">bodyMassIndexGrouped</a>({ ...params }) -> Junction.GroupedBodyMassIndexResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.bodyMassIndexGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.BodyMassIndexGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">basalBodyTemperatureGrouped</a>({ ...params }) -> Junction.GroupedBasalBodyTemperatureResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.basalBodyTemperatureGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.BasalBodyTemperatureGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">handwashingGrouped</a>({ ...params }) -> Junction.GroupedHandwashingResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.handwashingGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.HandwashingGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">daylightExposureGrouped</a>({ ...params }) -> Junction.GroupedDaylightExposureResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.daylightExposureGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.DaylightExposureGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">uvExposureGrouped</a>({ ...params }) -> Junction.GroupedUvExposureResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.uvExposureGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.UvExposureGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">fallGrouped</a>({ ...params }) -> Junction.GroupedFallResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.fallGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.FallGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">inhalerUsageGrouped</a>({ ...params }) -> Junction.GroupedInhalerUsageResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.inhalerUsageGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.InhalerUsageGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">peakExpiratoryFlowRateGrouped</a>({ ...params }) -> Junction.GroupedPeakExpiratoryFlowRateResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.peakExpiratoryFlowRateGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.PeakExpiratoryFlowRateGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">forcedVitalCapacityGrouped</a>({ ...params }) -> Junction.GroupedForcedVitalCapacityResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.forcedVitalCapacityGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.ForcedVitalCapacityGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">forcedExpiratoryVolume1Grouped</a>({ ...params }) -> Junction.GroupedForcedExpiratoryVolume1Response</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.forcedExpiratoryVolume1Grouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.ForcedExpiratoryVolume1GroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">wheelchairPushGrouped</a>({ ...params }) -> Junction.GroupedWheelchairPushResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.wheelchairPushGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.WheelchairPushGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">sleepBreathingDisturbanceGrouped</a>({ ...params }) -> Junction.GroupedSleepBreathingDisturbanceResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.sleepBreathingDisturbanceGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.SleepBreathingDisturbanceGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">sleepApneaAlertGrouped</a>({ ...params }) -> Junction.GroupedSleepApneaAlertResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.sleepApneaAlertGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.SleepApneaAlertGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">standDurationGrouped</a>({ ...params }) -> Junction.GroupedStandDurationResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.standDurationGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.StandDurationGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">standHourGrouped</a>({ ...params }) -> Junction.GroupedStandHourResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.standHourGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.StandHourGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">heartRateAlertGrouped</a>({ ...params }) -> Junction.GroupedHeartRateAlertResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.heartRateAlertGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.HeartRateAlertGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">afibBurdenGrouped</a>({ ...params }) -> Junction.GroupedAFibBurdenResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.afibBurdenGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.AfibBurdenGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">workoutDurationGrouped</a>({ ...params }) -> Junction.GroupedWorkoutDurationResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.workoutDurationGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.WorkoutDurationGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">vo2MaxGrouped</a>({ ...params }) -> Junction.GroupedVo2MaxResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.vo2MaxGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.Vo2MaxGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">stressLevelGrouped</a>({ ...params }) -> Junction.GroupedStressLevelResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.stressLevelGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.StressLevelGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">mindfulnessMinutesGrouped</a>({ ...params }) -> Junction.GroupedMindfulnessMinutesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.mindfulnessMinutesGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.MindfulnessMinutesGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">caffeineGrouped</a>({ ...params }) -> Junction.GroupedCaffeineResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.caffeineGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.CaffeineGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">waterGrouped</a>({ ...params }) -> Junction.GroupedWaterResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.waterGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.WaterGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">stepsGrouped</a>({ ...params }) -> Junction.GroupedStepsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.stepsGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.StepsGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">floorsClimbedGrouped</a>({ ...params }) -> Junction.GroupedFloorsClimbedResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.floorsClimbedGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.FloorsClimbedGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">distanceGrouped</a>({ ...params }) -> Junction.GroupedDistanceResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.distanceGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.DistanceGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">caloriesBasalGrouped</a>({ ...params }) -> Junction.GroupedCaloriesBasalResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.caloriesBasalGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.CaloriesBasalGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">caloriesActiveGrouped</a>({ ...params }) -> Junction.GroupedCaloriesActiveResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.caloriesActiveGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.CaloriesActiveGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">respiratoryRateGrouped</a>({ ...params }) -> Junction.GroupedRespiratoryRateResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.respiratoryRateGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.RespiratoryRateGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">noteGrouped</a>({ ...params }) -> Junction.GroupedNoteResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.noteGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.NoteGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">insulinInjectionGrouped</a>({ ...params }) -> Junction.GroupedInsulinInjectionResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.insulinInjectionGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.InsulinInjectionGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">igeGrouped</a>({ ...params }) -> Junction.GroupedIgeResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.igeGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.IgeGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">iggGrouped</a>({ ...params }) -> Junction.GroupedIggResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.iggGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.IggGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">hypnogramGrouped</a>({ ...params }) -> Junction.GroupedHypnogramResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.hypnogramGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.HypnogramGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">hrvGrouped</a>({ ...params }) -> Junction.GroupedHrvResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.hrvGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.HrvGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">heartrateGrouped</a>({ ...params }) -> Junction.GroupedHeartRateResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.heartrateGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.HeartrateGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">glucoseGrouped</a>({ ...params }) -> Junction.GroupedGlucoseResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.glucoseGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GlucoseGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">cholesterolGrouped</a>({ ...params }) -> Junction.GroupedCholesterolResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.cholesterolGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.CholesterolGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">carbohydratesGrouped</a>({ ...params }) -> Junction.GroupedCarbohydratesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.carbohydratesGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.CarbohydratesGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">bodyTemperatureDeltaGrouped</a>({ ...params }) -> Junction.GroupedBodyTemperatureDeltaResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.bodyTemperatureDeltaGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.BodyTemperatureDeltaGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">bodyTemperatureGrouped</a>({ ...params }) -> Junction.GroupedBodyTemperatureResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.bodyTemperatureGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.BodyTemperatureGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">bodyWeightGrouped</a>({ ...params }) -> Junction.GroupedBodyWeightResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.bodyWeightGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.BodyWeightGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">bodyFatGrouped</a>({ ...params }) -> Junction.GroupedBodyFatResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.bodyFatGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.BodyFatGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">bloodOxygenGrouped</a>({ ...params }) -> Junction.GroupedBloodOxygenResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.bloodOxygenGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.BloodOxygenGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">electrocardiogramVoltageGrouped</a>({ ...params }) -> Junction.GroupedElectrocardiogramVoltageResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.electrocardiogramVoltageGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.ElectrocardiogramVoltageGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">bloodPressureGrouped</a>({ ...params }) -> Junction.GroupedBloodPressureResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.bloodPressureGrouped({
    userId: "user_id",
    cursor: "cursor",
    nextCursor: "next_cursor",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.BloodPressureGroupedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">vo2Max</a>({ ...params }) -> Junction.ClientFacingVo2MaxTimeseries[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.vo2Max({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.Vo2MaxVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">stressLevel</a>({ ...params }) -> Junction.ClientFacingStressLevelTimeseries[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.stressLevel({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.StressLevelVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">mindfulnessMinutes</a>({ ...params }) -> Junction.ClientFacingMindfulnessMinutesTimeseries[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.mindfulnessMinutes({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.MindfulnessMinutesVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">caffeine</a>({ ...params }) -> Junction.ClientFacingCaffeineTimeseries[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.caffeine({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.CaffeineVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">water</a>({ ...params }) -> Junction.ClientFacingWaterTimeseries[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.water({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.WaterVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">steps</a>({ ...params }) -> Junction.ClientFacingStepsTimeseries[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.steps({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.StepsVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">floorsClimbed</a>({ ...params }) -> Junction.ClientFacingFloorsClimbedTimeseries[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.floorsClimbed({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.FloorsClimbedVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">distance</a>({ ...params }) -> Junction.ClientFacingDistanceTimeseries[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.distance({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.DistanceVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">caloriesBasal</a>({ ...params }) -> Junction.ClientFacingCaloriesBasalTimeseries[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.caloriesBasal({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.CaloriesBasalVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">caloriesActive</a>({ ...params }) -> Junction.ClientFacingCaloriesActiveTimeseries[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.caloriesActive({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.CaloriesActiveVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">respiratoryRate</a>({ ...params }) -> Junction.ClientFacingRespiratoryRateTimeseries[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.respiratoryRate({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.RespiratoryRateVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">ige</a>({ ...params }) -> Junction.ClientFacingIgeTimeseries[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.ige({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.IgeVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">igg</a>({ ...params }) -> Junction.ClientFacingIggTimeseries[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.igg({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.IggVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">hypnogram</a>({ ...params }) -> Junction.ClientFacingHypnogramTimeseries[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.hypnogram({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.HypnogramVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">hrv</a>({ ...params }) -> Junction.ClientFacingHrvTimeseries[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.hrv({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.HrvVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">heartrate</a>({ ...params }) -> Junction.ClientFacingHeartRateTimeseries[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.heartrate({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.HeartrateVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">glucose</a>({ ...params }) -> Junction.ClientFacingGlucoseTimeseries[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.glucose({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GlucoseVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">cholesterolTriglycerides</a>({ ...params }) -> Junction.ClientFacingCholesterolTimeseries[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.cholesterolTriglycerides({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.CholesterolTriglyceridesVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">cholesterolTotal</a>({ ...params }) -> Junction.ClientFacingCholesterolTimeseries[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.cholesterolTotal({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.CholesterolTotalVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">cholesterolLdl</a>({ ...params }) -> Junction.ClientFacingCholesterolTimeseries[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.cholesterolLdl({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.CholesterolLdlVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">cholesterolHdl</a>({ ...params }) -> Junction.ClientFacingCholesterolTimeseries[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.cholesterolHdl({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.CholesterolHdlVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">cholesterol</a>({ ...params }) -> Junction.ClientFacingCholesterolTimeseries[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.cholesterol({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.CholesterolVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">bodyWeight</a>({ ...params }) -> Junction.ClientFacingBodyWeightTimeseries[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.bodyWeight({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.BodyWeightVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">bodyFat</a>({ ...params }) -> Junction.ClientFacingBodyFatTimeseries[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.bodyFat({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.BodyFatVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">bloodOxygen</a>({ ...params }) -> Junction.ClientFacingBloodOxygenTimeseries[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.bloodOxygen({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.BloodOxygenVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">electrocardiogramVoltage</a>({ ...params }) -> Junction.ClientFacingElectrocardiogramVoltageTimeseries[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.electrocardiogramVoltage({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.ElectrocardiogramVoltageVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="/src/api/resources/vitals/client/Client.ts">bloodPressure</a>({ ...params }) -> Junction.ClientFacingBloodPressureTimeseries[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.vitals.bloodPressure({
    userId: "user_id",
    provider: "provider",
    startDate: "start_date",
    endDate: "end_date"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.BloodPressureVitalsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VitalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## User
<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">getAll</a>({ ...params }) -> Junction.PaginatedUsersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET All users for team.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.getAll({
    offset: 1,
    limit: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetAllUserRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `UserClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">create</a>({ ...params }) -> Junction.ClientFacingUser</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

POST Create a Vital user given a client_user_id and returns the user_id.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.create({
    clientUserId: "client_user_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.UserCreateBody` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `UserClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">getTeamMetrics</a>() -> Junction.MetricsResult</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET metrics for team.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.getTeamMetrics();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `UserClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">getConnectedProviders</a>({ ...params }) -> Record&lt;string, Junction.ClientFacingProviderWithStatus[]&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET Users connected providers
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.getConnectedProviders({
    userId: "user_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetConnectedProvidersUserRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `UserClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">getLatestUserInfo</a>({ ...params }) -> Junction.UserInfo</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.getLatestUserInfo({
    userId: "user_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetLatestUserInfoUserRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `UserClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">createInsurance</a>({ ...params }) -> Junction.ClientFacingInsurance</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.createInsurance({
    userId: "user_id",
    payorCode: "payor_code",
    memberId: "member_id",
    relationship: "Self",
    insured: {
        firstName: "first_name",
        lastName: "last_name",
        gender: "female",
        address: {
            firstLine: "first_line",
            country: "country",
            zip: "zip",
            city: "city",
            state: "state"
        },
        dob: "dob",
        email: "email",
        phoneNumber: "phone_number"
    }
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.CreateInsuranceRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `UserClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">getLatestInsurance</a>({ ...params }) -> Junction.ClientFacingInsurance</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.getLatestInsurance({
    userId: "user_id",
    isPrimary: true
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetLatestInsuranceUserRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `UserClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">upsertUserInfo</a>({ ...params }) -> Junction.UserInfo</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.upsertUserInfo({
    userId: "user_id",
    firstName: "first_name",
    lastName: "last_name",
    email: "email",
    phoneNumber: "phone_number",
    gender: "gender",
    dob: "dob",
    address: {
        firstLine: "first_line",
        country: "country",
        zip: "zip",
        city: "city",
        state: "state"
    }
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.UserInfoCreateRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `UserClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">getByClientUserId</a>({ ...params }) -> Junction.ClientFacingUser</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET user_id from client_user_id.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.getByClientUserId({
    clientUserId: "client_user_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetByClientUserIdUserRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `UserClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">deregisterProvider</a>({ ...params }) -> Junction.UserSuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.deregisterProvider({
    userId: "user_id",
    provider: "oura"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.DeregisterProviderUserRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `UserClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">get</a>({ ...params }) -> Junction.ClientFacingUser</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.get({
    userId: "user_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetUserRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `UserClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">delete</a>({ ...params }) -> Junction.UserSuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.delete({
    userId: "user_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.DeleteUserRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `UserClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">patch</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.patch({
    userId: "user_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.UserPatchBody` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `UserClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">undoDelete</a>({ ...params }) -> Junction.UserSuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.undoDelete({
    userId: "user_id",
    clientUserId: "client_user_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.UndoDeleteUserRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `UserClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">refresh</a>({ ...params }) -> Junction.UserRefreshSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Trigger a manual refresh for a specific user
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.refresh({
    userId: "user_id",
    timeout: 1.1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.RefreshUserRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `UserClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">getDevices</a>({ ...params }) -> Junction.ClientFacingDevice[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.getDevices({
    userId: "user_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetDevicesUserRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `UserClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">getDevice</a>({ ...params }) -> Junction.ClientFacingDevice</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.getDevice({
    userId: "user_id",
    deviceId: "device_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetDeviceUserRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `UserClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">getUserSignInToken</a>({ ...params }) -> Junction.UserSignInTokenResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.getUserSignInToken({
    userId: "user_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetUserSignInTokenUserRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `UserClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">createPortalUrl</a>({ ...params }) -> Junction.CreateUserPortalUrlResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.createPortalUrl({
    userId: "user_id",
    context: "launch"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.CreateUserPortalUrlBody` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `UserClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Team
<details><summary><code>client.team.<a href="/src/api/resources/team/client/Client.ts">get</a>({ ...params }) -> Junction.ClientFacingTeam</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get team.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.team.get({
    teamId: "team_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetTeamRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TeamClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.team.<a href="/src/api/resources/team/client/Client.ts">getUserById</a>({ ...params }) -> Junction.ClientFacingUser[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Search team users by user_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.team.getUserById({
    queryId: "query_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetUserByIdTeamRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TeamClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.team.<a href="/src/api/resources/team/client/Client.ts">getSvixUrl</a>() -> Record&lt;string, unknown&gt;</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.team.getSvixUrl();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `TeamClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.team.<a href="/src/api/resources/team/client/Client.ts">getSourcePriorities</a>({ ...params }) -> Record&lt;string, unknown&gt;[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET source priorities.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.team.getSourcePriorities({
    dataType: "workouts"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetSourcePrioritiesTeamRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TeamClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.team.<a href="/src/api/resources/team/client/Client.ts">updateSourcePriorities</a>() -> Record&lt;string, unknown&gt;[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Patch source priorities.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.team.updateSourcePriorities();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `TeamClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.team.<a href="/src/api/resources/team/client/Client.ts">getPhysicians</a>({ ...params }) -> Junction.ClientFacingPhysician[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.team.getPhysicians({
    teamId: "team_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetPhysiciansTeamRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TeamClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Providers
<details><summary><code>client.providers.<a href="/src/api/resources/providers/client/Client.ts">getAll</a>({ ...params }) -> Junction.ClientFacingProviderDetailed[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get Provider list
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.providers.getAll({
    sourceType: "source_type"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetAllProvidersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProvidersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Introspect
<details><summary><code>client.introspect.<a href="/src/api/resources/introspect/client/Client.ts">getUserResources</a>({ ...params }) -> Junction.UserResourcesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.introspect.getUserResources({
    userId: "user_id",
    provider: "oura",
    userLimit: 1,
    cursor: "cursor",
    nextCursor: "next_cursor"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetUserResourcesIntrospectRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `IntrospectClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.introspect.<a href="/src/api/resources/introspect/client/Client.ts">getUserHistoricalPulls</a>({ ...params }) -> Junction.UserHistoricalPullsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.introspect.getUserHistoricalPulls({
    userId: "user_id",
    provider: "oura",
    userLimit: 1,
    cursor: "cursor",
    nextCursor: "next_cursor"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetUserHistoricalPullsIntrospectRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `IntrospectClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## LabTests
<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">get</a>({ ...params }) -> Junction.ClientFacingLabTest[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET all the lab tests the team has access to.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.get({
    generationMethod: "auto",
    labSlug: "lab_slug",
    collectionMethod: "testkit",
    status: "active",
    markerIds: [1],
    providerIds: ["provider_ids"],
    name: "name",
    orderKey: "price",
    orderDirection: "asc"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetLabTestsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">create</a>({ ...params }) -> Junction.ClientFacingLabTest</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.create({
    name: "name",
    method: "testkit",
    description: "description"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.CreateLabTestRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">getById</a>({ ...params }) -> Junction.ClientFacingLabTest</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET all the lab tests the team has access to.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.getById({
    labTestId: "lab_test_id",
    labAccountId: "lab_account_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetByIdLabTestsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">updateLabTest</a>({ ...params }) -> Junction.ClientFacingLabTest</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.updateLabTest({
    labTestId: "lab_test_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.UpdateLabTestRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">getMarkers</a>({ ...params }) -> Junction.GetMarkersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List active and orderable markers for a given Lab. Note that reflex markers are not included.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.getMarkers({
    labId: [1],
    labSlug: "lab_slug",
    name: "name",
    aLaCarteEnabled: true,
    labAccountId: "lab_account_id",
    page: 1,
    size: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetMarkersLabTestsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">getMarkersForOrderSet</a>({ ...params }) -> Junction.GetMarkersResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.getMarkersForOrderSet({
    page: 1,
    size: 1,
    body: {}
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetMarkersForOrderSetLabTestsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">getMarkersForLabTest</a>({ ...params }) -> Junction.GetMarkersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all markers for a given Lab Test, as well as any associated reflex markers.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.getMarkersForLabTest({
    labTestId: "lab_test_id",
    labAccountId: "lab_account_id",
    page: 1,
    size: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetMarkersForLabTestLabTestsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">getMarkersByLabAndProviderId</a>({ ...params }) -> Junction.ClientFacingMarker</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET a specific marker for the given lab and provider_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.getMarkersByLabAndProviderId({
    providerId: "provider_id",
    labId: 1,
    labAccountId: "lab_account_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetMarkersByLabAndProviderIdLabTestsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">getLabs</a>() -> Junction.ClientFacingLab[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET all the labs.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.getLabs();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">getPaginated</a>({ ...params }) -> Junction.LabTestResourcesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET lab tests the team has access to as a paginated list.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.getPaginated({
    labTestLimit: 1,
    nextCursor: "next_cursor",
    generationMethod: "auto",
    labSlug: "lab_slug",
    collectionMethod: "testkit",
    status: "active",
    markerIds: [1],
    providerIds: ["provider_ids"],
    name: "name",
    orderKey: "price",
    orderDirection: "asc"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetPaginatedLabTestsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">getLabTestCollectionInstructionPdf</a>({ ...params }) -> core.BinaryResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.getLabTestCollectionInstructionPdf({
    labTestId: "lab_test_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetLabTestCollectionInstructionPdfLabTestsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">getOrders</a>({ ...params }) -> Junction.GetOrdersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET many orders with filters.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.getOrders({
    searchInput: "search_input",
    startDate: new Date("2024-01-15T09:30:00.000Z"),
    endDate: new Date("2024-01-15T09:30:00.000Z"),
    updatedStartDate: new Date("2024-01-15T09:30:00.000Z"),
    updatedEndDate: new Date("2024-01-15T09:30:00.000Z"),
    status: ["ordered"],
    orderKey: "created_at",
    orderDirection: "asc",
    orderType: ["testkit"],
    isCritical: true,
    interpretation: "normal",
    orderActivationTypes: ["current"],
    userId: "user_id",
    patientName: "patient_name",
    shippingRecipientName: "shipping_recipient_name",
    orderIds: ["order_ids"],
    orderTransactionId: "order_transaction_id",
    page: 1,
    size: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetOrdersLabTestsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">getPhlebotomyAppointmentAvailability</a>({ ...params }) -> Junction.AppointmentAvailabilitySlots</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return the available time slots to book an appointment with a phlebotomist
for the given address and order.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.getPhlebotomyAppointmentAvailability({
    startDate: "start_date",
    body: {
        firstLine: "first_line",
        city: "city",
        state: "state",
        zipCode: "zip_code"
    }
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetPhlebotomyAppointmentAvailabilityLabTestsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">bookPhlebotomyAppointment</a>({ ...params }) -> Junction.ClientFacingAppointment</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Book an at-home phlebotomy appointment.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.bookPhlebotomyAppointment({
    orderId: "order_id",
    body: {
        bookingKey: "booking_key"
    }
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.BookPhlebotomyAppointmentLabTestsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">requestPhlebotomyAppointment</a>({ ...params }) -> Junction.ClientFacingAppointment</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Request an at-home phlebotomy appointment.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.requestPhlebotomyAppointment({
    orderId: "order_id",
    address: {
        firstLine: "first_line",
        city: "city",
        state: "state",
        zipCode: "zip_code"
    },
    provider: "getlabs"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.RequestAppointmentRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">reschedulePhlebotomyAppointment</a>({ ...params }) -> Junction.ClientFacingAppointment</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Reschedule a previously booked at-home phlebotomy appointment.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.reschedulePhlebotomyAppointment({
    orderId: "order_id",
    body: {
        bookingKey: "booking_key"
    }
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.ReschedulePhlebotomyAppointmentLabTestsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">cancelPhlebotomyAppointment</a>({ ...params }) -> Junction.ClientFacingAppointment</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Cancel a previously booked at-home phlebotomy appointment.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.cancelPhlebotomyAppointment({
    orderId: "order_id",
    cancellationReasonId: "cancellation_reason_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.ApiApiV1EndpointsVitalApiLabTestingOrdersHelpersAppointmentCancelRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">getPhlebotomyAppointmentCancellationReason</a>() -> Junction.ClientFacingAppointmentCancellationReason[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get the list of reasons for cancelling an at-home phlebotomy appointment.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.getPhlebotomyAppointmentCancellationReason();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">getPhlebotomyAppointment</a>({ ...params }) -> Junction.ClientFacingAppointment</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get the appointment associated with an order.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.getPhlebotomyAppointment({
    orderId: "order_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetPhlebotomyAppointmentLabTestsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">getAreaInfo</a>({ ...params }) -> Junction.AreaInfo</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET information about an area with respect to lab-testing.

Information returned:
* Whether a given zip code is served by our Phlebotomy network.
* List of Lab locations in the area.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.getAreaInfo({
    zipCode: "zip_code",
    radius: "10",
    lab: "quest",
    labs: ["quest"],
    labAccountId: "lab_account_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetAreaInfoLabTestsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">getPscInfo</a>({ ...params }) -> Junction.PscInfo</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.getPscInfo({
    zipCode: "zip_code",
    labId: 1,
    radius: "10",
    capabilities: ["stat"],
    labAccountId: "lab_account_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetPscInfoLabTestsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">getOrderPscInfo</a>({ ...params }) -> Junction.PscInfo</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.getOrderPscInfo({
    orderId: "order_id",
    radius: "10",
    capabilities: ["stat"]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetOrderPscInfoLabTestsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">getResultPdf</a>({ ...params }) -> core.BinaryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint returns the lab results for the order.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.getResultPdf({
    orderId: "order_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetResultPdfLabTestsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">getResultMetadata</a>({ ...params }) -> Junction.LabResultsMetadata</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return metadata related to order results, such as lab metadata,
provider and sample dates.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.getResultMetadata({
    orderId: "order_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetResultMetadataLabTestsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">getResultRaw</a>({ ...params }) -> Junction.LabResultsRaw</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return both metadata and raw json test data
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.getResultRaw({
    orderId: "order_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetResultRawLabTestsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">getLabelsPdf</a>({ ...params }) -> core.BinaryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint returns the printed labels for the order.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.getLabelsPdf({
    orderId: "order_id",
    collectionDate: new Date("2024-01-15T09:30:00.000Z")
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetLabelsPdfLabTestsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">getPscAppointmentAvailability</a>({ ...params }) -> Junction.AppointmentAvailabilitySlots</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.getPscAppointmentAvailability({
    lab: "quest",
    startDate: "start_date",
    siteCodes: ["site_codes"],
    zipCode: "zip_code",
    radius: "10",
    allowStale: true
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetPscAppointmentAvailabilityLabTestsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">bookPscAppointment</a>({ ...params }) -> Junction.ClientFacingAppointment</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.bookPscAppointment({
    orderId: "order_id",
    body: {
        bookingKey: "booking_key"
    }
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.BookPscAppointmentLabTestsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">reschedulePscAppointment</a>({ ...params }) -> Junction.ClientFacingAppointment</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.reschedulePscAppointment({
    orderId: "order_id",
    body: {
        bookingKey: "booking_key"
    }
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.ReschedulePscAppointmentLabTestsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">cancelPscAppointment</a>({ ...params }) -> Junction.ClientFacingAppointment</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.cancelPscAppointment({
    orderId: "order_id",
    cancellationReasonId: "cancellationReasonId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.VitalCoreClientsLabTestGetlabsSchemaAppointmentCancelRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">getPscAppointmentCancellationReason</a>() -> Junction.ClientFacingAppointmentCancellationReason[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.getPscAppointmentCancellationReason();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">getPscAppointment</a>({ ...params }) -> Junction.ClientFacingAppointment</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get the appointment associated with an order.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.getPscAppointment({
    orderId: "order_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetPscAppointmentLabTestsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">getOrderCollectionInstructionPdf</a>({ ...params }) -> core.BinaryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET collection instructions for an order
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.getOrderCollectionInstructionPdf({
    orderId: "order_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetOrderCollectionInstructionPdfLabTestsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">getOrderRequistionPdf</a>({ ...params }) -> core.BinaryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET requisition pdf for an order
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.getOrderRequistionPdf({
    orderId: "order_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetOrderRequistionPdfLabTestsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">getOrderAbnPdf</a>({ ...params }) -> core.BinaryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET ABN pdf for an order
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.getOrderAbnPdf({
    orderId: "order_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetOrderAbnPdfLabTestsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">getOrder</a>({ ...params }) -> Junction.ClientFacingOrder</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET individual order by ID.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.getOrder({
    orderId: "order_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetOrderLabTestsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">createOrder</a>({ ...params }) -> Junction.PostOrderResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.createOrder({
    userId: "user_id",
    patientDetails: {
        firstName: "first_name",
        lastName: "last_name",
        dob: "dob",
        gender: "female",
        phoneNumber: "phone_number",
        email: "email"
    },
    patientAddress: {
        firstLine: "first_line",
        city: "city",
        state: "state",
        zip: "zip",
        country: "country"
    }
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.CreateOrderRequestCompatible` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">importOrder</a>({ ...params }) -> Junction.PostOrderResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.importOrder({
    userId: "user_id",
    billingType: "client_bill",
    orderSet: {},
    collectionMethod: "testkit",
    patientDetails: {
        firstName: "first_name",
        lastName: "last_name",
        dob: "dob",
        gender: "female",
        phoneNumber: "phone_number",
        email: "email"
    },
    patientAddress: {
        receiverName: "receiver_name",
        firstLine: "first_line",
        city: "city",
        state: "state",
        zip: "zip",
        country: "country"
    },
    sampleId: "sample_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.ImportOrderBody` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">cancelOrder</a>({ ...params }) -> Junction.PostOrderResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

POST cancel order
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.cancelOrder({
    orderId: "order_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.CancelOrderLabTestsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">simulateOrderProcess</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get available test kits.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.simulateOrderProcess({
    orderId: "order_id",
    finalStatus: "received.walk_in_test.ordered",
    delay: 1,
    body: {}
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.SimulateOrderProcessLabTestsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">updateOnSiteCollectionOrderDrawCompleted</a>({ ...params }) -> Junction.PostOrderResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

PATCH update on site collection order when draw is completed
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.updateOnSiteCollectionOrderDrawCompleted({
    orderId: "order_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.UpdateOnSiteCollectionOrderDrawCompletedLabTestsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labTests.<a href="/src/api/resources/labTests/client/Client.ts">validateIcdCodes</a>({ ...params }) -> Junction.ValidateIcdCodesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labTests.validateIcdCodes({
    codes: ["codes"]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.ValidateIcdCodesBody` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabTestsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Compendium
<details><summary><code>client.compendium.<a href="/src/api/resources/compendium/client/Client.ts">search</a>({ ...params }) -> Junction.SearchCompendiumResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.compendium.search({
    mode: "canonical"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.SearchCompendiumBody` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CompendiumClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.compendium.<a href="/src/api/resources/compendium/client/Client.ts">convert</a>({ ...params }) -> Junction.ConvertCompendiumResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.compendium.convert({
    targetLab: "labcorp"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.ConvertCompendiumBody` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CompendiumClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## LabAccount
<details><summary><code>client.labAccount.<a href="/src/api/resources/labAccount/client/Client.ts">getTeamLabAccounts</a>({ ...params }) -> Junction.GetTeamLabAccountsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labAccount.getTeamLabAccounts({
    labAccountId: "lab_account_id",
    status: "active"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetTeamLabAccountsLabAccountRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabAccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## OrderTransaction
<details><summary><code>client.orderTransaction.<a href="/src/api/resources/orderTransaction/client/Client.ts">getTransaction</a>({ ...params }) -> Junction.GetOrderTransactionResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.orderTransaction.getTransaction({
    transactionId: "transaction_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetTransactionOrderTransactionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrderTransactionClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.orderTransaction.<a href="/src/api/resources/orderTransaction/client/Client.ts">getTransactionResult</a>({ ...params }) -> Junction.LabResultsRaw</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.orderTransaction.getTransactionResult({
    transactionId: "transaction_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetTransactionResultOrderTransactionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrderTransactionClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.orderTransaction.<a href="/src/api/resources/orderTransaction/client/Client.ts">getTransactionResultPdf</a>({ ...params }) -> core.BinaryResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.orderTransaction.getTransactionResultPdf({
    transactionId: "transaction_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetTransactionResultPdfOrderTransactionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrderTransactionClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Testkit
<details><summary><code>client.testkit.<a href="/src/api/resources/testkit/client/Client.ts">register</a>({ ...params }) -> Junction.PostOrderResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.testkit.register({
    sampleId: "sample_id",
    patientDetails: {
        firstName: "first_name",
        lastName: "last_name",
        dob: "dob",
        gender: "female",
        phoneNumber: "phone_number",
        email: "email"
    },
    patientAddress: {
        firstLine: "first_line",
        city: "city",
        state: "state",
        zip: "zip",
        country: "country"
    }
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.RegisterTestkitRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TestkitClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.testkit.<a href="/src/api/resources/testkit/client/Client.ts">createOrder</a>({ ...params }) -> Junction.PostOrderResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates an order for an unregistered testkit
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.testkit.createOrder({
    userId: "user_id",
    labTestId: "lab_test_id",
    shippingDetails: {
        receiverName: "receiver_name",
        firstLine: "first_line",
        city: "city",
        state: "state",
        zip: "zip",
        country: "country",
        phoneNumber: "phone_number"
    }
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.CreateRegistrableTestkitOrderRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TestkitClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Order
<details><summary><code>client.order.<a href="/src/api/resources/order/client/Client.ts">resendEvents</a>({ ...params }) -> Junction.ResendWebhookResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Replay a webhook for a given set of orders
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.order.resendEvents();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.ResendWebhookBody` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrderClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Insurance
<details><summary><code>client.insurance.<a href="/src/api/resources/insurance/client/Client.ts">searchGetPayorInfo</a>({ ...params }) -> Junction.ClientFacingPayorSearchResponse[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.insurance.searchGetPayorInfo({
    insuranceName: "insurance_name",
    provider: "change_healthcare",
    providerPayorId: "provider_payor_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.SearchGetPayorInfoInsuranceRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `InsuranceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.insurance.<a href="/src/api/resources/insurance/client/Client.ts">searchPayorInfo</a>({ ...params }) -> Junction.ClientFacingPayorSearchResponseDeprecated[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.insurance.searchPayorInfo();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.PayorSearchRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `InsuranceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.insurance.<a href="/src/api/resources/insurance/client/Client.ts">searchDiagnosis</a>({ ...params }) -> Junction.ClientFacingDiagnosisInformation[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.insurance.searchDiagnosis({
    diagnosisQuery: "diagnosis_query"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.SearchDiagnosisInsuranceRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `InsuranceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Payor
<details><summary><code>client.payor.<a href="/src/api/resources/payor/client/Client.ts">createPayor</a>({ ...params }) -> Junction.ClientFacingPayor</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.payor.createPayor({
    name: "name",
    address: {
        firstLine: "first_line",
        country: "country",
        zip: "zip",
        city: "city",
        state: "state"
    }
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.CreatePayorBody` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PayorClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## LabReport
<details><summary><code>client.labReport.<a href="/src/api/resources/labReport/client/Client.ts">parserCreateJob</a>({ ...params }) -> Junction.ParsingJob</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a parse job, uploads the file(s) to provider, persists the job row,
and starts the ParseLabReport. Returns a generated job_id.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labReport.parserCreateJob({
    file: [fs.createReadStream("/path/to/your/file")],
    userId: "user_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.CreateLabReportParserJobBody` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabReportClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.labReport.<a href="/src/api/resources/labReport/client/Client.ts">parserGetJob</a>({ ...params }) -> Junction.ParsingJob</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieves the parse job status and stored result if completed.

Returns:
    ParseLabResultJobResponse with job status and parsed data (if complete)
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.labReport.parserGetJob({
    jobId: "job_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.ParserGetJobLabReportRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LabReportClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Aggregate
<details><summary><code>client.aggregate.<a href="/src/api/resources/aggregate/client/Client.ts">queryOne</a>({ ...params }) -> Junction.AggregationResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.aggregate.queryOne({
    userId: "user_id",
    timeframe: {
        type: "relative",
        anchor: "anchor",
        past: {
            unit: "minute"
        }
    },
    queries: [{
            select: [{
                    arg: {
                        sleep: "id"
                    },
                    func: "mean"
                }]
        }]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.QueryBatch` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AggregateClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.aggregate.<a href="/src/api/resources/aggregate/client/Client.ts">getResultTableForContinuousQuery</a>({ ...params }) -> Junction.AggregationResult</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.aggregate.getResultTableForContinuousQuery({
    userId: "user_id",
    queryIdOrSlug: "query_id_or_slug"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetResultTableForContinuousQueryAggregateRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AggregateClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.aggregate.<a href="/src/api/resources/aggregate/client/Client.ts">getTaskHistoryForContinuousQuery</a>({ ...params }) -> Junction.ContinuousQueryTaskHistoryResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.aggregate.getTaskHistoryForContinuousQuery({
    userId: "user_id",
    queryIdOrSlug: "query_id_or_slug",
    nextCursor: "next_cursor",
    limit: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Junction.GetTaskHistoryForContinuousQueryAggregateRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AggregateClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

