# GUI

**자바 GUI 특징**

**✓ 강력한 GUI 컴포넌트 제공**

**✓ 쉬운 GUI 프로그래밍**

&#x20;

**자바의 GUI 프로그래밍 방법**

**✓ GUI 컴포넌트 이용**

**- AWT 패키지와 Swing 패키지**

**- AWT**

&#x20; . java.awt패키지

**- Swing**

&#x20; .javax.swing 패키지

**- JavaFX**

&#x20; . JAVA 11에서 제거 (CORBA, Java EE, Java FX, 애플릿, 자바 웹 스타트 기능)



**Swing 컴포넌트 예시**

* **JButton**
* **JCheckBox**
* **JRadioButton**
* **JTextField**
* **JPassewordField**
* **JTextArea**
* **JComboBox**
* **JList**
* **JProgeressBar**
* **JTooTip**
* **JScrollPane**
* **JMenu**
* **JDialog**
* **JFrame**

이 밖에도 JApplet, JTable, JTree, JEditorPane, JTextPane, JToolBar, JSplitPane, JTabbedPane 등 여러 가지의 컴포넌트가 있다.



**컨테이너와 컴포넌트**

**✓ 컨테이너**

\- 다른 컴포넌트를 포함할 수 있는 GUI 컴포넌트

\- 다른 컨테이너에 포함될 수 있음

&#x20; . AWT 컨테이너: Panel, Frame, Applet, Dialog, Window

&#x20; . Swing 컨테이너: JPanel, JFrame, JApplet, JDialog, JWindow

&#x20;

**✓ 컴포넌트**

\- 컨테이너에 포함되어야 비로소 화면에 출력될 수 있는 GUI 객체

\- 다른 컴포넌트를 포함할 수 없는 순수 컴포넌트

\- 모든 GUI 컴포넌트가 상속받는 클래스: java.awt.Compnent

\- 스윙 컴포넌트가 상속받는 클래스: javax.swing.JComponent



**GUI 작성 절차**

**1) 컨테이너를 생성한다.**

**2) 컴포넌트를 추가한다.**

****

**JFrame 컨테이너 클래스**

**✓ Swing 클래스 계층구조**

**- Component**

&#x20; . 화면에 표시되어서 사용자와 상호 작용하는 시각적인 객체를 나타냄.

**- Container**

&#x20; . 내부에 다른 컴포넌트를 추가할 수 있는 기능을 제공

&#x20; . 이 클래스의 add()를 사용하면 컨테이너 안에 컴포넌트를 추가

**- Window**

&#x20; . 경계선, 타이틀 바, 버튼을 가지고 있는 윈도우를 정의

**- Frame**

&#x20; . 자바 GUI 애플리케이션의 기초(AWT)

**- JFrame**

&#x20; . Frame 클래스를 스윙의 출시에 맞추어 변경

&#x20;

**FlowLayout 배치 관리자**

**✓ 배치관리자를 지정하지 않으면 묵시적으로 FlowLayout으로 지정한다.**

**✓ 컴포넌트를 수평 방향으로 배치하는 관리자**

&#x20; \- 왼쪽에서 오른쪽, 위에서 아래로 순차적으로 배열

&#x20; \- if) 한 줄에 모두 배치하지 못한다면 다음 줄에 연속하여 배열

![](<../../.gitbook/assets/image (1).png>)



**BorderLayout 배치 관리자**

**✓ 컴포넌트를 추가할 때 방향을 지정하여 추가할 수 있는 기능을 제공**

**✓ 배치 방향: 동, 서, 남, 북, 중앙**

&#x20;  \- East(LINE\_END), West(LINE\_START)

&#x20;  \- South(PAGE\_END), North(PAGE\_START), Center

**✓ 배치 방법**

&#x20;  **-** add(Component comp, int index) //comp를 index의 공간에 배치

**✓ 생성자**

&#x20;  \- BorderLayout()

&#x20;  \- BorderLayout(int hGap, int vGap)

**✓ add() 메소드**

&#x20;  \- void add(Component comp, int index)

![](<../../.gitbook/assets/image (2).png>)



**GridLayout 배치 관리자**

**✓ 컴포넌트를 행과 열을 가진 배열 형태로 배치**

**✓ 컨테이너 공간을 동일한 사각형 격자(그리드)로 분할하고 각 셀에 컴포넌트 하나씩 배치**

&#x20;  \- 생성자에 행수와 열수 지정

&#x20;  \- 셀에 왼쪽에서 오른쪽으로, 다시 위에서 아래로 순서대로 배치

**✓ 생성자**

&#x20;  \- GridLayout()

&#x20;  \- GridLayout(int row, int cols)

&#x20;  \- GridLayout(int rows, int cols, int hgap, int vgap)

![](<../../.gitbook/assets/image (3).png>)
