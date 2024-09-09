
import webcolors

def get_color_name(hex_code):
    try:
        color_name = webcolors.hex_to_name(hex_code)
    except ValueError:
        color_name = "Unknown color"
    return color_name

def get_rgb_from_hex(hex_code):
    try:
        rgb = webcolors.hex_to_rgb(hex_code)
    except ValueError:
        rgb = (0, 0, 0)
    return rgb

def main():
    while True:
        hex_code = input("Enter a hex color code (e.g., #ff5733) or 'exit' to quit: ")
        if hex_code.lower() == 'exit':
            break
        color_name = get_color_name(hex_code)
        rgb = get_rgb_from_hex(hex_code)
        
        print(f"Color Name: {color_name}")
        print(f"RGB Value: {rgb}")

if __name__ == "__main__":
    main()
