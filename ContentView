import SwiftUI

struct RotateView: View {
    @State var degree1 = 0.0
    @State var degree2 = 0.0
    @State var degree3 = 0.0
    var body: some View {
        Spacer(minLength: 50)
        Text("Rotational Symmetry 旋轉對稱")
            .font(.system(size: 64))
        HStack(spacing: 100) {
            VStack {
            Spacer()
            Image("Image1")
                .resizable()
                .aspectRatio(contentMode: .fit)
                .frame(height: 300)
                .opacity(0.5)
                .overlay(Image("Image1")
                            .resizable()
                            .aspectRatio(contentMode: .fit)
                            .frame(height: 300)
                            .opacity(1)
                            .rotationEffect(Angle.degrees(degree1))
                            .gesture(
                                RotationGesture()
                                    .onChanged { angle in self.degree1 = angle.degrees}
                                    .onEnded { angle in self.degree1 = angle.degrees}
                            )
                            )
            Text("Rotation: " + String(round(degree1)))
            Spacer()
        }
            VStack {
            Spacer()
            Image("Image2")
                .resizable()
                .aspectRatio(contentMode: .fit)
                .frame(height: 300)
                .opacity(0.5)
                .overlay(Image("Image2")
                            .resizable()
                            .aspectRatio(contentMode: .fit)
                            .frame(height: 300)
                            .opacity(1)
                            .rotationEffect(Angle.degrees(degree2))
                            .gesture(
                                RotationGesture()
                                    .onChanged { angle in self.degree2 = angle.degrees}
                                    .onEnded { angle in self.degree2 = angle.degrees}
                            )
                )
            Text("Rotation: " + String(round(degree2)))
            Spacer()
        }
        VStack {
            Spacer()
            Image("Image3")
                .resizable()
                .aspectRatio(contentMode: .fit)
                .frame(height: 300)
                .opacity(0.5)
                .overlay(Image("Image3")
                            .resizable()
                            .aspectRatio(contentMode: .fit)
                            .frame(height: 300)
                            .opacity(1)
                            .rotationEffect(Angle.degrees(degree3))
                            .gesture(
                                RotationGesture()
                                    .onChanged { angle in self.degree3 = angle.degrees}
                                    .onEnded { angle in self.degree3 = angle.degrees}
                            )
                )
            Text("Rotation: " + String(round(degree3)))
            Spacer()
        }
        }
        Button(action: {
            degree1 = 0.0
            degree2 = 0.0
            degree3 = 0.0
        }){
            Text("Reset")
                .font(.title)
                .padding()
                .background(Color.black)
                .cornerRadius(20)
        }
    }
}

struct RotateView_Previews: PreviewProvider {
    static var previews: some View {
        RotateView()
    }
}

