---
title: 테스트용
permalink: /test/test-a/
author_profile: false
sidebar:
  nav: "test"
---

#ReactNative Permission

1.코드 인데 적용은되냐?
```javascript
    export const requestPermission = ():AppThunk => async dispatch => {
    let result
    if(Platform.OS === 'ios'){
        result = await requestMultiple([
            PERMISSIONS.IOS.CAMERA,
            PERMISSIONS.IOS.PHOTO_LIBRARY,
            PERMISSIONS.IOS.LOCATION_WHEN_IN_USE
        ])
    } else {
        result = await requestMultiple([
            PERMISSIONS.ANDROID.CAMERA,
            PERMISSIONS.ANDROID.READ_EXTERNAL_STORAGE,
            PERMISSIONS.ANDROID.ACCESS_FINE_LOCATION,
            PERMISSIONS.ANDROID.WRITE_EXTERNAL_STORAGE
        ])
    }
    console.log(result,'ㅙㅠㅣ')
    dispatch(setPermission(result))
    return result
    // return new Promise((resolve => ))
}
```



