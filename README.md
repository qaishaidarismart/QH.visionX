import React from 'react';
import { View, Text, StyleSheet, TouchableOpacity, Linking } from 'react-native';

export default function App() {
  const links = [
    { name: "وب‌سایت", url: "https://www.qaishaiderismart.af" },
    { name: "لینک‌های من", url: "https://linktr.ee/qhvisionx" },
    { name: "ربات هوشمند", url: "https://monica.im/share/bot?botId=Uv8FNqyH" },
    { name: "کدهای من روی GitHub", url: "https://github.com/qaishaidarismart" },
    { name: "رزومه آنلاین", url: "https://cv.qaishaiderismart.af" }
  ];

  return (
    <View style={styles.container}>
      <Text style={styles.title}>QH-Smart</Text>
      <Text style={styles.subtitle}>قیس حیدری هوشمند</Text>

      {links.map((item, index) => (
        <TouchableOpacity
          key={index}
          style={styles.button}
          onPress={() => Linking.openURL(item.url)}
        >
          <Text style={styles.buttonText}>{item.name}</Text>
        </TouchableOpacity>
      ))}
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
    alignItems: 'center',
    backgroundColor: '#f5f5f5',
    padding: 20,
  },
  title: {
    fontSize: 32,
    fontWeight: 'bold',
    color: '#1e3a8a',
    marginBottom: 10,
  },
  subtitle: {
    fontSize: 18,
    color: '#4b5563',
    marginBottom: 40,
    textAlign: 'center',
  },
  button: {
    backgroundColor: '#1e3a8a',
    paddingVertical: 15,
    paddingHorizontal: 30,
    borderRadius: 10,
    marginVertical: 10,
    width: '90%',
    alignItems: 'center',
  },
  buttonText: {
    color: 'white',
    fontSize: 16,
    fontWeight: '600',
  },
});
