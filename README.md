











# Desafio Dio - Construindo um App usando Sensor de Movimento com React Native**

## 

###### 

# Dio-flashlight

Desafio dio: Construindo um app usando o sensor de movimento com React Native

![image](https://user-images.githubusercontent.com/28990749/165650549-07daaabe-15fa-432e-9146-71bae90e43b0.png)

![image](https://user-images.githubusercontent.com/28990749/165650568-afdd77ea-fa79-488c-ac0b-13c9ecce847c.png)


## Conteúdo 

- Libs react-native-shake e react-native-torch
- icons: https://drive.google.com/drive/folders/1aDTyA09EFjFvqmXqkDKLoMhFx65QQExQ
- StyleSheet
- Hook useState
- Hook useEffect
- Add Listener to RNShake
- Lifecicly ReactJS



### *Desafio*

Criar um aplicativo que use o sensor de movimento do celular para controlar o volume de um áudio.

- *Consultas e Resultados*
- O sensor de movimento do celular pode ser usado para detectar movimentos como inclinação, rotação e aceleração.
- O volume de um áudio pode ser controlado usando o método `setVolume()` do objeto `AudioContext`.
- O aplicativo pode ser criado usando a biblioteca React Native, que é uma plataforma de desenvolvimento para criar aplicativos móveis nativos para iOS e Android.
- *Exploração*

O sensor de movimento do celular pode ser usado para criar aplicativos de várias funcionalidades, como:

- Um aplicativo que controla o volume de um áudio ao inclinar o celular.
- Um aplicativo que muda a cor de um objeto ao girá-lo.
- Um aplicativo que cria um efeito de vibração ao sacudir o celular.

**Requisitos:**

1. O aplicativo deve ser capaz de acessar e interpretar os dados do sensor de movimento do dispositivo.
2. A funcionalidade do aplicativo deve ser diretamente influenciada pelos dados do sensor de movimento. Por exemplo, um jogo que usa a inclinação do dispositivo para mover um personagem.
3. O aplicativo deve ser desenvolvido utilizando React Native, permitindo que seja usado tanto em dispositivos Android quanto iOS.

**Consultas e Resultados:**

1. **Consulta:** Iniciar o aplicativo **Resultado:** O aplicativo inicia e começa a monitorar os dados do sensor de movimento.
2. **Consulta:** Mover o dispositivo **Resultado:** O aplicativo responde ao movimento do dispositivo de alguma maneira, dependendo da funcionalidade específica do aplicativo.

### **Resumo Didático:**

Neste desafio, você irá desenvolver um aplicativo móvel utilizando React Native que faz uso do sensor de movimento do dispositivo. React Native é uma estrutura popular para o desenvolvimento de aplicativos móveis, pois permite que você escreva código uma vez e o execute em várias plataformas, incluindo Android e iOS.

O sensor de movimento do dispositivo pode fornecer dados valiosos sobre como o dispositivo está sendo manipulado pelo usuário. Isso pode ser usado para criar uma variedade de experiências interativas, desde jogos que respondem à inclinação do dispositivo até aplicativos de fitness que rastreiam os movimentos do usuário.

Ao completar este desafio, você terá ganhado experiência prática com o desenvolvimento de aplicativos móveis interativos usando React Native e sensores de movimento

O sensor de movimento do celular é uma ferramenta poderosa que pode ser usada para criar aplicativos de várias funcionalidades. A biblioteca React Native é uma ótima opção para desenvolver aplicativos móveis nativos para iOS e Android.

Espero que este desafio tenha sido útil para você aprender mais sobre o sensor de movimento do celular e sobre o React Native.



## **PODE SE FAZER POR CÓDIGO TAMÉM:**

Aqui está o código do aplicativo no React Native que usa o sensor de movimento:

plaintext

![Done](chrome-extension://igpdmclhhlcpoindmhkhillbfhdgoegm/b3baca6de20012788f7d.svg)![Copy](chrome-extension://igpdmclhhlcpoindmhkhillbfhdgoegm/7120b68615ebe4b28075.svg)

```plaintext
import React, { useState } from "react";
import { View, Text, StyleSheet } from "react-native";
import * as RNSensors from "react-native-sensors";

export default function App() {
  const [roll, setRoll] = useState(0);
  const [pitch, setPitch] = useState(0);

  useEffect(() => {
    // Obtém uma referência ao sensor de movimento
    const accelerometer = RNSensors.Accelerometer.create();

    // Registra um observador para o sensor de movimento
    accelerometer.subscribe((data) => {
      // Atualiza os valores da inclinação e da rotação
      setRoll(data.roll);
      setPitch(data.pitch);
    });

    // Desregistra o observador quando o componente for desmontável
    return () => accelerometer.unsubscribe();
  }, []);

  return (
    <View style={styles.container}>
      <Text style={styles.text}>Inclinação: {roll}</Text>
      <Text style={styles.text}>Rotação: {pitch}</Text>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: "center",
    alignItems: "center",
  },
  text: {
    fontSize: 20,
    margin: 10,
  },
});
```

Este código cria um aplicativo simples que mostra os valores da inclinação e da rotação do celular. Para isso, ele usa a biblioteca `react-native-sensors` para obter uma referência ao sensor de movimento e registrar um observador para o sensor. Quando o observador recebe um novo valor do sensor, ele atualiza os valores da inclinação e da rotação no aplicativo.

## **Outra Opção de Codigo:**

.

o desafio de construir um app de lanterna com React Native que utiliza o sensor de movimento do celular. Vamos dividir o projeto em módulos e fornecer exemplos práticos.

**Módulo 1: Configuração do Ambiente** Antes de começar, é necessário configurar o ambiente de desenvolvimento para React Native. Isso inclui a instalação do Node.js, Watchman, React Native CLI e Android Studio ou Xcode para emulação.

**Módulo 2: Criação do Projeto** Utilize o comando `react-native init NomeDoProjeto` para criar um novo projeto React Native. Isso criará a estrutura básica do projeto para você começar a trabalhar.

**Módulo 3: Implementação da Interface** Desenvolva a interface do usuário (UI) do app de lanterna. Isso pode incluir um botão para ligar e desligar a lanterna e um indicador visual que mostra se a lanterna está ligada ou não.

**Módulo 4: Integração com o Sensor de Movimento** Para detectar o movimento de chacoalhar, você pode usar a biblioteca `react-native-sensors` que fornece acesso aos sensores do dispositivo¹[3](https://github.com/react-native-sensors/react-native-sensors). Você precisará monitorar os dados do acelerômetro para detectar um padrão de chacoalhada.

**Módulo 5: Controle da Lanterna** Para controlar a lanterna do dispositivo, você pode usar a API nativa do dispositivo. No Android, isso é feito através do `CameraManager`, enquanto no iOS, você usará o `AVFoundation`.

**Módulo 6: Testes e Depuração** Teste o app em diferentes dispositivos para garantir que a lanterna acende corretamente ao tocar na tela e ao chacoalhar o celular. Use ferramentas de depuração para resolver quaisquer problemas que surgirem.

**Exemplo Prático:**

```
import { Vibration, TouchableOpacity } from 'react-native';
import Torch from 'react-native-torch';
import RNShake from 'react-native-shake';

class App extends Component {
  componentDidMount() {
    RNShake.addEventListener('ShakeEvent', () => {
      // Liga a lanterna ao chacoalhar o celular
      Torch.switchState(true);
      Vibration.vibrate(500); // Feedback tátil
    });
  }

  componentWillUnmount() {
    RNShake.removeEventListener('ShakeEvent');
  }

  handlePress = () => {
    // Liga ou desliga a lanterna ao tocar na tela
    Torch.switchState(!this.state.isTorchOn);
    this.setState({ isTorchOn: !this.state.isTorchOn });
  };

  render() {
    return (
      <TouchableOpacity onPress={this.handlePress} style={styles.container}>
        {/* UI do App */}
      </TouchableOpacity>
    );
  }
}
```



Este código é um exemplo simplificado. Ele mostra como você pode ligar a lanterna ao chacoalhar o celular e ao tocar na tela. Lembre-se de ajustar o código conforme necessário para o seu projeto específico e realizar testes adequados.

O App de lanterna é um projeto interessante que combina a funcionalidade prática de uma lanterna com a detecção de movimento usando React Native. Vou detalhar mais sobre o funcionamento e os recursos desse aplicativo:

**Funcionalidades Principais:**

- **Ligar/Desligar Lanterna:** O usuário pode controlar a lanterna do celular tocando na tela, o que é uma funcionalidade básica de qualquer app de lanterna.
- **Detecção de Movimento:** A característica única deste app é a capacidade de acender a lanterna ao detectar o movimento específico de chacoalhar o celular. Isso é possível através do uso de sensores de movimento disponíveis no dispositivo.

**Tecnologias Utilizadas:**

- **React Native:** Uma framework para desenvolvimento de aplicativos móveis usando JavaScript e React, que permite criar uma experiência de usuário nativa tanto para Android quanto para iOS.
- **Bibliotecas de Sensores:** Para acessar e utilizar os sensores de movimento do dispositivo, são utilizadas bibliotecas como `react-native-sensors`¹[3](https://github.com/react-native-sensors/react-native-sensors), que facilitam a integração com o hardware do celular.

**Desenvolvimento do App:**

1. **Criação do Projeto:** Inicia-se com a configuração do ambiente de desenvolvimento e a criação do projeto React Native.
2. **Interface do Usuário:** Desenvolve-se a UI com componentes React Native, como botões e indicadores de status.
3. **Integração com Sensores:** Implementa-se a lógica para detecção de movimento, utilizando o acelerômetro do dispositivo para identificar quando o celular é chacoalhado.
4. **Controle da Lanterna:** Utiliza-se APIs nativas do sistema operacional para ligar e desligar a lanterna do dispositivo.
5. **Testes:** Realiza-se testes em diferentes dispositivos para assegurar que o app funcione corretamente em várias condições e modelos de celular.

**Exemplo de Código:**

```
import { Vibration, TouchableOpacity } from 'react-native';
import Torch from 'react-native-torch';
import RNShake from 'react-native-shake';

class App extends Component {
  // ... restante do código

  componentDidMount() {
    RNShake.addEventListener('ShakeEvent', () => {
      Torch.switchState(true); // Liga a lanterna ao chacoalhar
      Vibration.vibrate(500); // Feedback tátil
    });
  }

  // ... restante do código
}
```



Este trecho de código demonstra como você pode adicionar a funcionalidade de ligar a lanterna ao chacoalhar o celular. É importante notar que este é apenas um exemplo simplificado e que o desenvolvimento completo do app envolverá mais detalhes e funcionalidades.

Para mais informações e tutoriais sobre como criar um app de lanterna com React Native, você pode consultar recursos educacionais e vídeos disponíveis online²[1](https://www.dio.me/projects/construindo-um-app-usando-sensor-de-movimento-com-react-native)³[2](https://github.com/VagnerBellacosa/140_ConstruindoAppSensorMovimentoReactNative). Esses recursos podem oferecer uma visão mais aprofundada sobre o processo de desenvolvimento e as melhores práticas.

https://drive.google.com/drive/folders/1Kuh5tysH7-UFuSLHX0IQIIh2xcghHUIX?usp=sharing

https://github.com/ismaelsousa/dio-flashlight

https://docs.google.com/presentation/d/1zSHZ8xBvWNUv6ZY21fXr7UseLm5BVeSc/edit?usp=sharing&ouid=105300330738120646134&rtpof=true&sd=true
