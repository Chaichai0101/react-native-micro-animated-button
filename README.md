# react-native-micro-animated-button
<img src="https://raw.githubusercontent.com/sonaye/react-native-micro-animated-button/master/demo1.gif" width="400">
<img src="https://raw.githubusercontent.com/sonaye/react-native-micro-animated-button/master/demo2.gif" width="400">

# Installation
`yarn add react-native-micro-animated-button`

# Definition
```javascript
type button = {
  backgroundColor?: string,  // default = white
  bounce?: boolean,          // default = false
  errorColor: string,        // default = red
  errorIconColor?: string,   // default = white
  errorIconName: string,     // from FontAwesome
  foregroundColor?: string,  // default = black
  iconSize?: number,         // default = 17
  label: string,
  labelStyle?: Object,       // default = defaultLabelStyle
  maxWidth?: number,         // default = 240
  maxWidth?: number,         // default = 40
  onError?: Function,        // default = () => null
  onPress?: Function,        // default = () => null
  onSuccess?: Function,      // default = () => null
  renderIcon?: any,          // default = null
  renderIndicator?: any,     // default = null
  style?: Object,            // default = defaultStyle
  successColor?: string,     // default = green
  successIconColor?: string, // default = white
  successIconName: string    // from FontAwesome
};

const defaultStyle = {
  borderRadius: 25,
  borderWidth: 0.5,
  height: 40,
  marginBottom: 10,
  marginTop: 10
};

const defaultLabelStyle = {
  padding: 9
};
```

## Examples
```javascript
import React from 'react';
import { View } from 'react-native';

import Button from 'react-native-micro-animated-button';

const Example1 = () => (
  <View style={{ alignItems: 'center', flex: 1, justifyContent: 'center' }}>
    <Button
      bounce
      foregroundColor="#0f9d58"
      label="Submit"
      onPress={() => this.b1.success()}
      ref={ref => (this.b1 = ref)}
      successIconName="check"
    />

    <Button
      bounce
      foregroundColor="#4285f4"
      label="Retweet"
      onPress={() => this.b2.success()}
      ref={ref => (this.b2 = ref)}
      successIconName="retweet"
    />

    <Button
      bounce
      foregroundColor="#db4437"
      label="Favorite"
      onPress={() => this.b3.success()}
      ref={ref => (this.b3 = ref)}
      successIconName="heart"
    />
  </View>
);

const Example2 = () => (
  <View style={{ alignItems: 'center', flex: 1, justifyContent: 'center' }}>
    <Button
      bounce
      errorColor="#db4437"
      errorIconName="thumbs-down"
      foregroundColor="#9e9e9e"
      label="Am I even?"
      onPress={() => new Date().getSeconds() % 2 === 0 ? this.b1.success() : this.b1.error()}
      ref={ref => (this.b1 = ref)}
      successColor="#0f9d58"
      successIconName="thumbs-up"
    />

    <Button
      bounce
      errorColor="#db4437"
      errorIconName="thumbs-down"
      foregroundColor="#9e9e9e"
      label="Am I even?"
      onPress={() => new Date().getSeconds() % 2 === 0 ? this.b2.success() : this.b2.error()}
      ref={ref => (this.b2 = ref)}
      successColor="#0f9d58"
      successIconName="thumbs-up"
    />

    <Button
      bounce
      errorColor="#db4437"
      errorIconName="thumbs-down"
      foregroundColor="#9e9e9e"
      label="Am I even?"
      onPress={() => new Date().getSeconds() % 2 === 0 ? this.b3.success() : this.b3.error()}
      ref={ref => (this.b3 = ref)}
      successColor="#0f9d58"
      successIconName="thumbs-up"
    />
  </View>
);

export { Example1, Example 2 };
```
