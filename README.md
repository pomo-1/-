import streamlit as st

# 앱 제목
st.title("🍀 행운 낙찰 계산기")
st.write("핸드폰에서 바로 사용하는 입찰 분석기입니다.")

# 입력창
base_price = st.number_input("기초금액을 입력하세요 (원)", value=100000000)
rate = st.slider("희망 사정률 (%)", 97.0, 103.0, 100.0, 0.0001)

# 계산 결과
result = base_price * (rate / 100)

st.divider()
st.subheader("✅ 예상 투찰 금액")
st.header(f"{result:,.0f} 원")
st.caption(f"적용 사정률: {rate:.4f}%")
